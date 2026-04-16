# 2.10. Merge і Dissolve з буфером стандартного розміру

Отриманий вектор `#simplified` ділянок ПЗС із подвійним розміром доцільно об'єднати із буфером ПЗС стандартного розміру `#buffered`, алгоритмами **Merge** і **Dissolve**.

```yaml
{
  "area_units": "m2",
  "distance_units": "meters",
  "ellipsoid": "EPSG:7024",
  "inputs": {
    "CRS": null,
    "LAYERS": [
      "memory:../#simplified"
      "memory:../#buffered"
    ],
    "OUTPUT": "TEMPORARY_OUTPUT"
  }
}
```

![Merge](image_1771529588257_0.png)

```yaml
{
  "area_units": "m2",
  "distance_units": "meters",
  "ellipsoid": "EPSG:7024",
  "inputs": {
    "FIELD": [],
    "INPUT": "memory:../merged"
    "OUTPUT": "TEMPORARY_OUTPUT",
    "SEPARATE_DISJOINT": false
  }
}
```

![Dissolve](image_1771529628355_0.png)

> Опис алгоритмів:
>
> **Merge**: https://docs.qgis.org/3.40/en/docs/user_manual/processing_algs/qgis/vectorgeneral.html#qgismergevectorlayers  
> **Dissolve**: https://docs.qgis.org/3.40/en/docs/user_manual/processing_algs/qgis/vectorgeometry.html#qgisdissolve
