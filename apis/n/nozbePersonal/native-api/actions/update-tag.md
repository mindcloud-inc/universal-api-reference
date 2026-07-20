# Update Tag with Nozbe Personal

Updates an existing tag in Nozbe Personal.

## Endpoint

- **Method:** `PUT`
- **Path:** `/tags/:id`
- **Base URL:** `https://api4.nozbe.com/v1/api`
- **Official documentation:** [Update Tag](https://api4.nozbe.com/v1/api#/tags/putTagById)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `id` | path | `string` | yes |
| `name` | body | `string` | no |
| `team_id` | body | `string` | no |
| `color` | body | `string` | no |
| `icon` | body | `string` | no |
| `is_favorite` | body | `boolean` | no |
