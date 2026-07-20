# List Per Diem Rates by State with GSA Per Diem

Retrieves per diem rates from GSA Per Diem by state.

## Endpoint

- **Method:** `GET`
- **Path:** `/rates/state/:state/year/:year`
- **Base URL:** `https://api.gsa.gov/travel/perdiem/v2`
- **Official documentation:** [List Per Diem Rates by State](https://open.gsa.gov/api/perdiem/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `state` | path | `string` | yes | Two-letter destination state abbreviation. Maximum length: 2. |
| `year` | path | `string` | yes | Fiscal year of travel. GSA documents up to three years available. |
