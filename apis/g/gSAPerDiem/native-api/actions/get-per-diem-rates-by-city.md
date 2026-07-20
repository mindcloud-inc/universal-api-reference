# Get Per Diem Rates by City with GSA Per Diem

Retrieves per diem rates from GSA Per Diem by city.

## Endpoint

- **Method:** `GET`
- **Path:** `/rates/city/:city/state/:state/year/:year`
- **Base URL:** `https://api.gsa.gov/travel/perdiem/v2`
- **Official documentation:** [Get Per Diem Rates by City](https://open.gsa.gov/api/perdiem/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `city` | path | `string` | yes | Destination city. GSA says city and state names are case-insensitive. |
| `state` | path | `string` | yes | Two-letter destination state abbreviation. Maximum length: 2. |
| `year` | path | `string` | yes | Fiscal year of travel. GSA documents up to three years available. |
