# Update Issue with Supabugs

Updates an existing issue in Supabugs.

## Endpoint

- **Method:** `PUT`
- **Path:** `/issues/:id`
- **Base URL:** `https://api.supabugs.io/api/public/v1`
- **Official documentation:** [Update Issue](https://api.supabugs.io/api/public/v1/docs/index.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | Supabugs issue id. |
| `description` | body | `string` | no | Updated issue description. |
| `type` | body | `string` | no | Bug type id from List Bug Types. |
| `severity` | body | `string` | no | Bug severity id from List Bug Severities. |
| `priority` | body | `string` | no | Bug priority id from List Bug Priorities. |
| `status` | body | `string` | no | Bug status id from List Bug Statuses. |
