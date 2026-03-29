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

## Code instruction:
1. The 'scraping_krisha.py' runs in terminal with 'python scraping_krisha.py [numbers of pages to extract]'. After you get 'krisha_data_raw.csv'.
2. Run all cells in 'cleaning_preparing.ipynb' for 'krisha_data_raw.csv', the geocoding part is optional, it also takes all ot of time. You will get 'astana_real_estate_dataset.csv'.
3. The 'astana_real_estate_dataset.csv' is ready.
