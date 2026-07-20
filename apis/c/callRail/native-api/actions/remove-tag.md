# Remove Tag with CallRail

Deletes a tag from CallRail.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/v3/a/:account_id/tags/:tag_id.json`
- **Base URL:** `https://api.callrail.com`
- **Official documentation:** [Remove Tag](https://apidocs.callrail.com/#removing-a-tag)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `account_id` | path | `string` | yes |
| `tag_id` | path | `string` | yes |
