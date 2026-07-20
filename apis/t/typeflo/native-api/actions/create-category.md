# Create Category with Typeflo

Creates a new category in Typeflo.

## Endpoint

- **Method:** `POST`
- **Path:** `/admin/category`
- **Base URL:** `https://{subdomain}.typeflo.io/api/headless`
- **Official documentation:** [Create Category](https://typeflo.io/knowledge-base/headless-cms-admin-api-documentation)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | body | `string` | yes | The display name of the category. |
| `slug` | body | `string` | no | URL-friendly version of the category name. |
| `metadescription` | body | `string` | no | Meta description for the category. |
