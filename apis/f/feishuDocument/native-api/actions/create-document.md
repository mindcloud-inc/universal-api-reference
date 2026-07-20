# Create Document with Feishu Document

Creates a new document in Feishu Docs.

## Endpoint

- **Method:** `POST`
- **Path:** `/open-apis/docx/v1/documents`
- **Base URL:** `https://open.larksuite.com`
- **Official documentation:** [Create Document](https://open.larksuite.com/document/server-docs/docs/docs/docx-v1/document/create)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json; charset=utf-8` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `title` | body | `string` | no | Optional document title. Lark limits the title to 1-800 characters when provided. |
