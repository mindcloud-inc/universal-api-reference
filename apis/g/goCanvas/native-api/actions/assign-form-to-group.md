# Assign Form to Group with GoCanvas

## Endpoint

- **Method:** `POST`
- **Path:** `/groups/:groupId/forms`
- **Base URL:** `https://www.gocanvas.com/api/v3`
- **Official documentation:** [Assign Form to Group](https://api.gocanvas.com/api/v3/docs#assign-form-to-group)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `groupId` | path | `string` | yes | — |
| `id` | body | `number` | no | Provide this or Root Version ID. |
| `root_version_id` | body | `number` | no | Provide this or Form ID. Selects the latest published form version. |
| `send_notification` | body | `boolean` | no | Notify group members, subject to notification settings. Defaults to false. |
