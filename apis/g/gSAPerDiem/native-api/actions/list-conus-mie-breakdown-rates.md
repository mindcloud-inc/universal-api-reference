# List CONUS M&IE Breakdown Rates with GSA Per Diem

Retrieves CONUS M&IE breakdown rates from GSA Per Diem.

## Endpoint

- **Method:** `GET`
- **Path:** `/rates/conus/mie/:year`
- **Base URL:** `https://api.gsa.gov/travel/perdiem/v2`
- **Official documentation:** [List CONUS M&IE Breakdown Rates](https://open.gsa.gov/api/perdiem/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `year` | path | `string` | yes | Fiscal year of travel. GSA documents up to three years available. |
