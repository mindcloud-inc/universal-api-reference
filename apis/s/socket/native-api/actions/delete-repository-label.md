# Delete Repository Label with Socket

Deletes an existing repository label from Socket.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/orgs/:org_slug/repos/labels/:label_id`
- **Base URL:** `https://api.socket.dev/v0`
- **Official documentation:** [Delete Repository Label](https://docs.socket.dev/reference/deleteorgrepolabel)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `label_id` | path | `string` | yes |
