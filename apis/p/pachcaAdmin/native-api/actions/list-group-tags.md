# List Group Tags with Pachca (Admin)

Retrieves group tags from the Pachca Admin API.

## Endpoint

- **Method:** `GET`
- **Path:** `/group_tags`
- **Base URL:** `https://api.pachca.com/api/shared/v1`
- **Official documentation:** [List Group Tags](https://dev.pachca.com/api/group-tags/list)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `names[]` | query | `array<string>` | no |
| `limit` | query | `number` | no |
| `cursor` | query | `string` | no |
