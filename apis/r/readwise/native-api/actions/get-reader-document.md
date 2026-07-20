# Get Reader Document with Readwise

Retrieves a document from Readwise Reader.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v3/list/`
- **Base URL:** `https://readwise.io`
- **Official documentation:** [Get Reader Document](https://readwise.io/reader_api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | query | `string` | yes | Reader document ID to fetch. |
| `withHtmlContent` | query | `boolean` | no | Whether to include parsed HTML content in the response. |
| `withRawSourceUrl` | query | `boolean` | no | Whether to include the raw source URL in the response. |
