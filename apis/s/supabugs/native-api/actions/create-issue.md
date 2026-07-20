# Create Issue with Supabugs

Creates a new issue in Supabugs.

## Endpoint

- **Method:** `POST`
- **Path:** `/issues`
- **Base URL:** `https://api.supabugs.io/api/public/v1`
- **Official documentation:** [Create Issue](https://api.supabugs.io/api/public/v1/docs/index.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `title` | body | `string` | yes | Issue title. |
| `description` | body | `string` | yes | Issue description. |
| `type` | body | `string` | yes | Bug type id from List Bug Types. |
| `severity` | body | `string` | yes | Bug severity id from List Bug Severities. |
| `priority` | body | `string` | yes | Bug priority id from List Bug Priorities. |
