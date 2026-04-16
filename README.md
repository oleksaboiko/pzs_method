# pzs_method

This repository is scaffolded from the structure of `../geospatial_analysis_in_pg.pdf`, the working paper titled `Застосування геопросторового аналізу у публічному управлінні земельними ресурсами на місцевому рівні`.

The directory tree uses ASCII slugs for portability, while preserving the source document's section order and meaning.

## Structure Mapping

- `00_article_text/` -> `Текст статті`
- `01_explanatory_note/` -> `Задача методики (Пояснювальна записка проекту)`
- `02_method_description/` -> `Опис методики`
- `02_method_description/01_rationale_for_tools_and_source_data/` -> `Обгрунтування вибору інструментів та вихідних даних`
- `02_method_description/01_rationale_for_tools_and_source_data/01_measurement_units/` -> `Одиниці виміру`
- `02_method_description/01_rationale_for_tools_and_source_data/02_coordinate_system/` -> `Система координат`
- `02_method_description/01_rationale_for_tools_and_source_data/03_method_procedure/` -> `Процедура методики`
- `02_method_description/01_rationale_for_tools_and_source_data/04_analytical_approach/` -> `Вибір аналітичного підходу`
- `02_method_description/01_rationale_for_tools_and_source_data/05_application_tools/` -> `Вибір прикладних інструментів`
- `02_method_description/01_rationale_for_tools_and_source_data/06_method_quality/` -> `Якість запропонованої методики`
- `03_input_data/` -> `Вхідні дані`
- `03_input_data/01_aoi_vector/` -> `векторний полігон AOI #aoi_vector`
- `03_input_data/02_dem_raster/` -> `DEM ... #dem_raster`
- `03_input_data/03_bodies_raster/` -> `векторні геопросторові дані водних об'єктів ... #bodies_raster`
- `04_persistent_working_data_preparation/` -> `1. Підготовка і формування постійних робочих даних`
- `04_persistent_working_data_preparation/01_working_data_inventory/` -> `1.1. Перелік постійних робочих даних`
- `04_persistent_working_data_preparation/02_preparation_procedure/01_prepare_water_px_id_raster/` -> `1.2.1. Підготовка растру водних об'єктів #water_px_id_raster`
- `04_persistent_working_data_preparation/02_preparation_procedure/02_prepare_water_px_elev_raster/` -> `1.2.2. Підготовка растру висоти водних об'єктів #water_px_elev_raster`
- `04_persistent_working_data_preparation/02_preparation_procedure/03_prepare_distance_and_nearest_water_pixel_rasters/` -> `1.2.3. Підготовка растрів віддаленості ... #distance_raster / #nearest_water_pix_id_raster`
- `04_persistent_working_data_preparation/02_preparation_procedure/04_prepare_nearest_water_pixel_elevation_raster/` -> `1.2.4. Підготовка растру ... #nearest_water_pix_elev_raster`
- `05_bank_zone_slope_analysis/` -> `2. Визначення ухилів рельєфу берегових зон за допомогою растрової алгебри`
- `05_bank_zone_slope_analysis/01_required_rasters_and_operations/` -> `2.1. Потрібні растрові дані та операції`
- `05_bank_zone_slope_analysis/02_detect_slope_exceedance_in_standard_buffer/` -> `2.2. Розрахунок растру понаднормативних ухилів`
- `05_bank_zone_slope_analysis/03_identify_water_pixels_near_exceedance_points/` -> `2.3. Ідентифікація пікселів водних об'єктів`
- `05_bank_zone_slope_analysis/04_extract_unique_problem_water_pixel_ids/` -> `2.4. Raster layer unique values report`
- `05_bank_zone_slope_analysis/05_prepare_max_buffer_id_raster/` -> `2.5. Підготовка #nearest_water_pix_id_raster_in_50_m`
- `05_bank_zone_slope_analysis/06_join_slope_detection_table_to_water_centroids/` -> `2.6. Join #slope_detected_table to #water_px_id_vector`
- `05_bank_zone_slope_analysis/07_reclassify_max_buffer_raster/` -> `2.7. Reclassify by layer -> #pz_raster_in_50_meter`
- `05_bank_zone_slope_analysis/08_vectorize_result/01_reclassify_binary/` -> `2.8.1. Бінарна рекласифікація`
- `05_bank_zone_slope_analysis/08_vectorize_result/02_polygonize/` -> `2.8.2. Polygonize`
- `05_bank_zone_slope_analysis/09_simplify_polygonized_output/` -> `2.9. Simplify`
- `05_bank_zone_slope_analysis/10_merge_with_standard_buffer/` -> `2.10. Merge + Dissolve with standard buffer`
- `06_references/` -> `Список використаної літератури`
- `07_remarks/` -> `Зауваження`

## Notes

- The structure is intentionally content-first and mirrors the document rather than a software package layout.
- Leaf directories currently contain `.gitkeep` placeholders so the full scaffold is tracked from the first commit.
