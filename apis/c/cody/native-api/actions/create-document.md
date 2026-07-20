# Create Document with Cody

## Endpoint

- **Method:** `POST`
- **Path:** `/documents`
- **Base URL:** `https://getcody.ai/api/v1`
- **Official documentation:** [Create Document](https://developers.meetcody.ai/operation/operation-create-document)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | body | `string` | no | Document name. |
| `folder_id` | body | `string` | no | Id of the folder to create the document in. |
| `content` | body | `string` | no | Text or HTML document content, up to 768 KB. |
