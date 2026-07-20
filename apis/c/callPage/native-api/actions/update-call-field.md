# Update Call Field with CallPage

Updates a field on an existing call in CallPage.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/calls/{call}/fields/{field}`
- **Base URL:** `https://core.callpage.io/api/v1/external`
- **Official documentation:** [Update Call Field](https://callpage.github.io/documentation-rest/#update-field)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `call` | path | `number` | yes | The call identifier. |
| `field` | path | `number` | yes | The field identifier to update. |
| `value` | body | `string` | yes | The value to set for the field. |
