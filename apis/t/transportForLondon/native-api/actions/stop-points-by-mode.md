# Get Stop Points By Mode with Transport for London

Retrieves stop points for modes in Transport for London.

## Endpoint

- **Method:** `GET`
- **Path:** `/StopPoint/Mode/:modes`
- **Base URL:** `https://api.tfl.gov.uk`
- **Official documentation:** [Get Stop Points By Mode](https://api.tfl.gov.uk/swagger/ui/index.html#!/StopPoint/StopPoint_GetByMode)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `modes` | path | `string` | yes | Comma-separated mode names, such as tube,dlr,bus. |
