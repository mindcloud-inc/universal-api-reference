# Delete Tags with E2B

Deletes tags from templates in E2B.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/templates/tags`
- **Base URL:** `https://api.e2b.app`
- **Official documentation:** [Delete Tags](https://e2b.dev/docs/api-reference/tags/delete-tags)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | body | `string` | yes | Name of the template. |
| `tags[]` | body | `array<string>` | yes | Tags to delete. |
