# Update Tag with CallRail

Updates a tag in CallRail.

## Endpoint

- **Method:** `PUT`
- **Path:** `/v3/a/:account_id/tags/:tag_id.json`
- **Base URL:** `https://api.callrail.com`
- **Official documentation:** [Update Tag](https://apidocs.callrail.com/#updating-a-tag)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `account_id` | path | `string` | yes |
| `tag_id` | path | `string` | yes |
| `name` | body | `string` | no |
| `color` | body | `string` | no |
| `disabled` | body | `boolean` | no |
