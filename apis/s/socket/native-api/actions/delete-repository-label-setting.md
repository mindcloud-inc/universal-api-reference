# Delete Repository Label Setting with Socket

Deletes an existing repository label setting from Socket.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/orgs/:org_slug/repos/labels/:label_id/label-setting`
- **Base URL:** `https://api.socket.dev/v0`
- **Official documentation:** [Delete Repository Label Setting](https://docs.socket.dev/reference/deleteorgrepolabelsetting)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `label_id` | path | `string` | yes |
