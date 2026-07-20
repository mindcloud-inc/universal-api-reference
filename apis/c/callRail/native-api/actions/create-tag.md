# Create Tag with CallRail

Creates a tag in CallRail.

## Endpoint

- **Method:** `POST`
- **Path:** `/v3/a/:account_id/tags.json`
- **Base URL:** `https://api.callrail.com`
- **Official documentation:** [Create Tag](https://apidocs.callrail.com/#creating-a-tag)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `account_id` | path | `string` | yes |
| `name` | body | `string` | yes |
| `company_id` | body | `string` | no |
| `color` | body | `string` | no |
| `tag_level` | body | `string` | no |
