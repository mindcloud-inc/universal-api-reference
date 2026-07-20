# Get Line Status By Mode with Transport for London

Retrieves line status for modes in Transport for London.

## Endpoint

- **Method:** `GET`
- **Path:** `/Line/Mode/:modes/Status`
- **Base URL:** `https://api.tfl.gov.uk`
- **Official documentation:** [Get Line Status By Mode](https://api.tfl.gov.uk/swagger/ui/index.html#!/Line/Line_StatusByMode)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `modes` | path | `string` | yes | Comma-separated mode names, such as tube,dlr,bus. |
| `detail` | query | `boolean` | no | Set to true to include details of disruptions causing line status. |
