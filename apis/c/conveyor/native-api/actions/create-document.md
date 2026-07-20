# Create Document with Conveyor

Creates a document in the Conveyor exchange.

## Endpoint

- **Method:** `POST`
- **Path:** `/v2/exchange/documents`
- **Base URL:** `https://api.conveyor.com/api`
- **Official documentation:** [Create Document](https://docs.conveyor.com/reference/post-document)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `multipart/form-data` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | body | `string` | yes | Document name. |
| `file` | body | `file` | yes | Document file upload. |
| `description` | body | `string` | no | Document description. |
| `certification` | body | `string` | no | Document certification type. |
| `featured` | body | `boolean` | no | Whether the document is featured. |
| `folder_id` | body | `string` | no | Folder identifier to place the document in. |
| `access_level` | body | `string` | no | Document access level. |
| `product_line_ids` | body | `string<string>` | no | Product line identifiers for the document. |
| `access_group_ids` | body | `string<string>` | no | Access group identifiers for the document. |
| `disable_downloads` | body | `boolean` | no | Whether downloads are disabled. |
| `use_for_question_answering` | body | `boolean` | no | Whether to use the document for question answering. |
