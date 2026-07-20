# List Counties By State with Environmental Protection Agency

Retrieves counties for a state from EPA AQS.

## Endpoint

- **Method:** `GET`
- **Path:** `/list/countiesByState`
- **Base URL:** `https://aqs.epa.gov/data/api`
- **Official documentation:** [List Counties By State](https://aqs.epa.gov/aqsweb/documents/data_api.html#lists)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `state` | query | `string` | yes | Two-digit state FIPS code, including a leading zero when applicable. |
