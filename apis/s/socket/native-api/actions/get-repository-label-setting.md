# Get Repository Label Setting with Socket

Retrieves a repository label setting from Socket.

## Endpoint

- **Method:** `GET`
- **Path:** `/orgs/:org_slug/repos/labels/:label_id/label-setting`
- **Base URL:** `https://api.socket.dev/v0`
- **Official documentation:** [Get Repository Label Setting](https://docs.socket.dev/reference/getorgrepolabelsetting)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `label_id` | path | `string` | yes |
