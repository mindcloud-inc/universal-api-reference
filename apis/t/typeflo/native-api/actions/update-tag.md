# Update Tag with Typeflo

Updates an existing tag in Typeflo.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/admin/tags/:id`
- **Base URL:** `https://{subdomain}.typeflo.io/api/headless`
- **Official documentation:** [Update Tag](https://typeflo.io/knowledge-base/headless-cms-admin-api-documentation)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | The unique ID of the tag. |
| `name` | body | `string` | no | The display name of the tag. |
| `slug` | body | `string` | no | URL-friendly version of the tag name. |
| `metadescription` | body | `string` | no | Meta description for the tag. |
