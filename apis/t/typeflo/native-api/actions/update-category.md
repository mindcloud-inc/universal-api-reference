# Update Category with Typeflo

Updates an existing category in Typeflo.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/admin/category/:id`
- **Base URL:** `https://{subdomain}.typeflo.io/api/headless`
- **Official documentation:** [Update Category](https://typeflo.io/knowledge-base/headless-cms-admin-api-documentation)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | The unique ID of the category. |
| `name` | body | `string` | no | The display name of the category. |
| `slug` | body | `string` | no | URL-friendly version of the category name. |
| `metadescription` | body | `string` | no | Meta description for the category. |
