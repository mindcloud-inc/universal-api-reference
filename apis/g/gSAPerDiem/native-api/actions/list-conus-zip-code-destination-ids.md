# List CONUS ZIP Code Destination IDs with GSA Per Diem

Retrieves CONUS ZIP code destination IDs from GSA Per Diem.

## Endpoint

- **Method:** `GET`
- **Path:** `/rates/conus/zipcodes/:year`
- **Base URL:** `https://api.gsa.gov/travel/perdiem/v2`
- **Official documentation:** [List CONUS ZIP Code Destination IDs](https://open.gsa.gov/api/perdiem/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `year` | path | `string` | yes | Fiscal year of travel. GSA documents up to three years available. |
