# Create Tag with Typeflo

Creates a new tag in Typeflo.

## Endpoint

- **Method:** `POST`
- **Path:** `/admin/tags`
- **Base URL:** `https://{subdomain}.typeflo.io/api/headless`
- **Official documentation:** [Create Tag](https://typeflo.io/knowledge-base/headless-cms-admin-api-documentation)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | body | `string` | yes | The display name of the tag. |
| `slug` | body | `string` | no | URL-friendly version of the tag name. |
| `metadescription` | body | `string` | no | Meta description for the tag. |
