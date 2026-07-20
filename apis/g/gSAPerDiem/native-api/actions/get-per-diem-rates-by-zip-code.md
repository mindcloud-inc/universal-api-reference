# Get Per Diem Rates by ZIP Code with GSA Per Diem

Retrieves per diem rates from GSA Per Diem by ZIP code.

## Endpoint

- **Method:** `GET`
- **Path:** `/rates/zip/:zip/year/:year`
- **Base URL:** `https://api.gsa.gov/travel/perdiem/v2`
- **Official documentation:** [Get Per Diem Rates by ZIP Code](https://open.gsa.gov/api/perdiem/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `zip` | path | `string` | yes | Destination ZIP code. Maximum length: 5. |
| `year` | path | `string` | yes | Fiscal year of travel. GSA documents up to three years available. |
