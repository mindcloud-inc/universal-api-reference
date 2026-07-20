# Update Document with Runway

Updates a document in Runway.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/v1/documents/[:id]`
- **Base URL:** `https://api.dev.runwayml.com`
- **Official documentation:** [Update Document](https://docs.dev.runwayml.com/api#tag/Knowledge/paths/~1v1~1documents~1%7Bid%7D/patch)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `content` | body | `string` | no | New markdown or plain text content for the document. |
| `id` | path | `string` | yes | UUID of the document to update. |
| `name` | body | `string` | no | New name for the document. |
