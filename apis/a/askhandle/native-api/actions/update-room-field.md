# Update Room Field with AskHandle

Updates one AskHandle room field by label.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/rooms/:label/`
- **Base URL:** `https://dashboard.askhandle.com/api/v1`
- **Official documentation:** [Update Room Field](https://dashboard.askhandle.com/api/v1/docs/api_reference.html#room)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `label` | path | `string` | no | The room label. |
| `name` | body | `string` | no | Room name. |
