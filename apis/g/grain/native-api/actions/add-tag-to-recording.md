# Add Tag to Recording with Grain

Adds a tag to a recording in Grain.

## Endpoint

- **Method:** `PUT`
- **Path:** `/v2/recordings/:recording_id/tags`
- **Base URL:** `https://api.grain.com/_/public-api`
- **Official documentation:** [Add Tag to Recording](https://developers.grain.com/)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `recording_id` | path | `list<string>` | yes |
| `tag` | body | `string` | yes |
