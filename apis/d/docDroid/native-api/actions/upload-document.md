# Upload Document with DocDroid

Uploads a new document to DocDroid.

## Endpoint

- **Method:** `POST`
- **Path:** `/document`
- **Base URL:** `https://www.docdroid.com/api`
- **Official documentation:** [Upload Document](https://www.docdroid.com/apidocs)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `multipart/form-data` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `file` | body | `file` | yes | The file to upload. |
| `name` | body | `string` | no | Optional display name for the document. |
| `visibility` | body | `list` | no | Set the document visibility. Accepted values: `password`, `private`, `public`. |
| `type` | body | `list` | no | Optional document type. Accepted values: `document`, `presentation`. |
| `password` | body | `string` | no | Optional password when visibility is set to password. |
| `allow_download` | body | `boolean` | no | Whether downloads are allowed. |
| `allow_search_engines_index` | body | `boolean` | no | Whether search engines may index the document. |
| `allow_copy_text` | body | `boolean` | no | Whether copying text is allowed. |
| `allow_embed` | body | `list` | no | Set embed permissions for the document. Accepted values: `any`, `none`, `whitelist`. |
| `allow_embed_domains[]` | body | `array<string>` | no | Optional list of domains allowed to embed the document. |
