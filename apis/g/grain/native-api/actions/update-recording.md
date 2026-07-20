# Update Recording with Grain

Updates an existing recording in Grain.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/v2/recordings/:recording_id`
- **Base URL:** `https://api.grain.com/_/public-api`
- **Official documentation:** [Update Recording](https://developers.grain.com/)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `recording_id` | path | `list<string>` | yes |
| `title` | body | `string` | no |
