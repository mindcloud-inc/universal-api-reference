# Get Shift with Toast

Retrieves one labor shift by Toast GUID or external identifier.

## Endpoint

- **Method:** `GET`
- **Path:** `/labor/v1/shifts/:shiftId`
- **Base URL:** `{connection}`
- **API:** Labor
- **Official documentation:** [Get Shift](https://doc.toasttab.com/openapi/labor/operation/shiftsShiftIdGet/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `shiftId` | path | `string` | yes | The Toast GUID or external identifier of the shift. |
