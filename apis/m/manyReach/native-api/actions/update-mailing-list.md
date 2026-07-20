# Update Mailing List with ManyReach

Updates an existing mailing list in ManyReach.

## Endpoint

- **Method:** `PATCH`
- **Path:** `https://api.manyreach.com/api/v2/lists/:id`
- **Base URL:** `https://api.manyreach.com`
- **Official documentation:** [Update Mailing List](https://api.manyreach.com/api#v2/tag/list)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | no | List ID. |
| `title` | body | `string` | no | Updated list title. |
