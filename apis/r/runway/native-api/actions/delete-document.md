# Delete Document with Runway

Deletes a document from Runway.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/v1/documents/[:id]`
- **Base URL:** `https://api.dev.runwayml.com`
- **Official documentation:** [Delete Document](https://docs.dev.runwayml.com/api#tag/Knowledge/paths/~1v1~1documents~1%7Bid%7D/delete)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | UUID of the document to delete. |
