# Create Document with Runway

Creates a document in Runway.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/documents`
- **Base URL:** `https://api.dev.runwayml.com`
- **Official documentation:** [Create Document](https://docs.dev.runwayml.com/api#tag/Knowledge/paths/~1v1~1documents/post)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `content` | body | `string` | yes | Markdown or plain text document content. |
| `name` | body | `string` | yes | Descriptive name for the document. |
