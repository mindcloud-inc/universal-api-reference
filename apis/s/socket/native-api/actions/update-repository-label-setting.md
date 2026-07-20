# Update Repository Label Setting with Socket

Updates an existing repository label setting in Socket.

## Endpoint

- **Method:** `PUT`
- **Path:** `/orgs/:org_slug/repos/labels/:label_id/label-setting`
- **Base URL:** `https://api.socket.dev/v0`
- **Official documentation:** [Update Repository Label Setting](https://docs.socket.dev/reference/updateorgrepolabelsetting)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `label_id` | path | `string` | yes |
