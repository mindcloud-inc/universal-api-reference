# Get Units By MAR ID And Type with Open Data DC

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v2.2/units/:marid/:type`
- **Base URL:** `https://datagate.dc.gov/mar/open`
- **Official documentation:** [Get Units By MAR ID And Type](https://datagate.dc.gov/mar/open/swagger/v2.2/swagger.json)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `marid` | path | `string` | yes | MAR identifier. |
| `type` | path | `string` | yes | Unit type. |
