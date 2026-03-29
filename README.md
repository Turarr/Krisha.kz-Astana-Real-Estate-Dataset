# Krisha.kz Astana Real Estate Dataset

## 📊 Astana Real Estate Dataset – Column Description
| Column Name             | Data Type | Description                                                                                        |
| ----------------------- | --------- | -------------------------------------------------------------------------------------------------- |
| **url**                 | object    | Link to the apartment listing on krisha.kz. Unique identifier for each advertisement.              |
| **title**               | object    | Raw listing title containing number of rooms, area (m²), floor information, and address.           |
| **price**               | int64     | Apartment price in Kazakhstani tenge (KZT).                                                        |
| **security**            | object    | Security features of the building (e.g., intercom, video surveillance, concierge, security guard). |
| **ceiling_height**      | float64   | Ceiling height in meters.                                                                          |
| **year_of_construction**       | int64     | Year the building was constructed.                                                                 |
| **district**            | object    | Administrative district of Astana where the apartment is located (e.g., Есильский, Сарыаркинский). |
| **residential_complex** | object    | Name of the residential complex (ЖК). If not specified, may contain default or generic values.     |
| **furnished**           | object    | Furnishing status of the apartment (e.g., fully furnished, without furniture).                     |
| **parking**             | object    | Parking availability (e.g., underground parking, yard parking, not specified).                     |
| **bathroom_type**       | object    | Bathroom configuration (e.g., combined, separate, 2+ bathrooms).                                   |
| **apartment_condition** | object    | Apartment renovation condition (e.g., fresh renovation, needs repair, not specified).              |
| **building_type**       | object    | Construction type of the building (e.g., brick, panel, monolithic).                                |
| **rooms**               | float64   | Number of rooms in the apartment.                                                                  |
| **current_floor**       | float64   | Floor on which the apartment is located.                                                           |
| **total_floors**        | float64   | Total number of floors in the building.                                                            |
| **area_m2**             | float64   | Total apartment area in square meters (m²).                                                        |
| **address**             | object    | Street name and house number of the apartment.                                                     |
| **district_lat**        | float64   | Latitude coordinate of the district center.                                                        |
| **district_lon**        | float64   | Longitude coordinate of the district center.                                                       |
| **apartment_lat**       | float64   | Latitude coordinate of the apartment location.                                                     |
| **apartment_lon**       | float64   | Longitude coordinate of the apartment location.                                                    |
| **coord_level**         | object    | Level of coordinate precision (e.g., district-level or exact apartment-level geolocation).         |

## 💻 Code Instruction:
1. The `scraping_krisha.py` runs in terminal with `python scraping_krisha.py [numbers of pages to extract]`. After you get `krisha_data_raw.csv`.
2. Run all cells in `cleaning_preparing.ipynb` for `krisha_data_raw.csv`, **the geocoding part is optional** `(just dont run process_data())` , it is also takes all ot of time. You will get `astana_real_estate_dataset.csv`.
4. The `astana_real_estate_dataset.csv` is ready.

## 📊 Sample From Dataset
| index | url                                                                        | title                                                                    | price     | security                          | ceiling_height | year_of_construction | district                               | residential_complex     | furnished  | parking             | bathroom_type | apartment_condition | building_type | rooms | current_floor | total_floors | area_m2 | address                        | district_lat | district_lon |
| ----- | -------------------------------------------------------------------------- | ------------------------------------------------------------------------ | --------- | --------------------------------- | -------------- | ------------- | -------------------------------------- | ----------------------- | ---------- | ------------------- | ------------- | ------------------- | ------------- | ----- | ------------- | ------------ | ------- | ------------------------------ | ------------ | ------------ |
| 4649  | [https://krisha.kz/a/show/1010768375](https://krisha.kz/a/show/1010768375) | 2-комнатная квартира · 40 м² · 6/12 этаж, Чингиз Айтматов 60             | 23990000  | домофон, видеонаблюдение          | 3.0            | 2022          | Есильский район, Астана, Казахстан     | Madrid                  | полностью  | паркинг             | совмещенный   | свежий ремонт       | кирпичный     | 2.0   | 6.0           | 12.0         | 40.0    | Чингиз Айтматов 60             | 51.12        | 71.43        |
| 4997  | [https://krisha.kz/a/show/1010565423](https://krisha.kz/a/show/1010565423) | 2-комнатная квартира · 45 м² · 3/5 этаж, Желтоксан 32/4                  | 16500000  | домофон, видеонаблюдение          | 2.9027         | 1962          | Астана, Казахстан                      | Панельный дом/Не указан | без мебели | Во дворе/не указано | совмещенный   | Не указано          | панельный     | 2.0   | 3.0           | 5.0          | 45.0    | Желтоксан 32/4                 | 51.133       | 71.433       |
| 2810  | [https://krisha.kz/a/show/696838397](https://krisha.kz/a/show/696838397)   | 5-комнатная квартира · 205.3 м² · 3/15 этаж, АзербайжанМамбетов 16       | 120000000 | охрана, видеонаблюдение, консьерж | 3.0            | 2008          | Сарыаркинский район, Астана, Казахстан | Алтын Орда              | полностью  | Во дворе/не указано | 2 с/у и более | Не указано          | монолитный    | 5.0   | 3.0           | 15.0         | 205.3   | АзербайжанМамбетов 16          | 51.17        | 71.41        |
| 3632  | [https://krisha.kz/a/show/1009082109](https://krisha.kz/a/show/1009082109) | 1-комнатная квартира · 40 м² · 9/16 этаж, Райымбек батыр 2 — Тауелсиздик | 35000000  | домофон, видеонаблюдение          | 3.0            | 2025          | Сарыаркинский район, Астана, Казахстан | Qasiet                  | полностью  | паркинг             | совмещенный   | свежий ремонт       | монолитный    | 1.0   | 9.0           | 16.0         | 40.0    | Райымбек батыр 2 — Тауелсиздик | 51.117       | 71.565       |
| 1372  | [https://krisha.kz/a/show/761883873](https://krisha.kz/a/show/761883873)   | 4-комнатная квартира · 136.55 м², Сагадат Нурмагамбетов 15, 16           | 105826250 | домофон, видеонаблюдение          | 3.0            | 2026          | Сарыаркинский район, Астана, Казахстан | Auez Park               | без мебели | Во дворе/не указано | 2 с/у и более | Не указано          | монолитный    | 4.0   | 6.0           | 11.0         | 136.55  | Сагадат Нурмагамбетов 15, 16   | 51.117       | 71.565       |
