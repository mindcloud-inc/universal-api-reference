# Remove Tag from Recording with Grain

Removes a tag from a recording in Grain.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/v2/recordings/:recording_id/tags/:tag`
- **Base URL:** `https://api.grain.com/_/public-api`
- **Official documentation:** [Remove Tag from Recording](https://developers.grain.com/)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `recording_id` | path | `list<string>` | yes |
| `tag` | path | `string` | yes |
