# Create Group with GoCanvas

## Endpoint

- **Method:** `POST`
- **Path:** `/groups`
- **Base URL:** `https://www.gocanvas.com/api/v3`
- **Official documentation:** [Create Group](https://api.gocanvas.com/api/v3/docs#create-a-group)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | body | `string` | no | — |
| `description` | body | `string` | no | — |
| `department_id` | body | `number` | no | When omitted, the current user's default department is used. |
