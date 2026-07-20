# Get Lines By Mode with Transport for London

Retrieves lines for selected modes in Transport for London.

## Endpoint

- **Method:** `GET`
- **Path:** `/Line/Mode/:modes`
- **Base URL:** `https://api.tfl.gov.uk`
- **Official documentation:** [Get Lines By Mode](https://api.tfl.gov.uk/swagger/ui/index.html#!/Line/Line_GetByMode)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `modes` | path | `string` | yes | Comma-separated mode names, such as tube,dlr,bus. |
