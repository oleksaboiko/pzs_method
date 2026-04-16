# 1.2.4. Підготовка растру висоти найближчого пікселя водного об'єкту `#nearest_water_pix_elev_raster`

- Вхідними даними для розрахунку є растр `#water_px_elev_raster`.
- Для роботи використовуємо алгоритм **r.grow.distance**, із результатів якого нам потрібен растр висоти найближчого об'єкту, а растр відстані може бути проігнорований, оскільки він є ідентичним вже отриманому растру `#distance_raster`.

Приклад налаштувань алгоритму:

```yaml
{
  "area_units": "m2",
  "distance_units": "meters",
  "ellipsoid": "EPSG:7024",
  "inputs": {
    "-m": false,
    "-n": false,
    "GRASS_RASTER_FORMAT_META": "",
    "GRASS_RASTER_FORMAT_OPT": "",
    "GRASS_REGION_CELLSIZE_PARAMETER": 0.0,
    "GRASS_REGION_PARAMETER": "numerical #dem extent [EPSG:given EPSG]",
    "distance": "TEMPORARY_OUTPUT",
    "input": "../#water_px_elev_raster.tif",,
    "metric": 0,
    "value": "../#nearest_water_pix_elev_raster.tif"
  }
}
```

![Nearest water pixel elevation raster](image_1771530532485_0.png)

> **Результат** - одноканальний растр значення ідентифікатора найближчого пікселя водного об'єкту `#nearest_water_pix_elev_raster`, зберігаємо в постійну пам'ять комп'ютера.
