# List Reader Documents with Readwise

Retrieves documents from the Readwise Reader library.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v3/list/`
- **Base URL:** `https://readwise.io`
- **Official documentation:** [List Reader Documents](https://readwise.io/reader_api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `updatedAfter` | query | `string` | no | Fetch only documents updated after this ISO 8601 datetime. |
| `category` | query | `string` | no | Filter documents by category. |
| `limit` | query | `number` | no | Maximum number of documents to return. |
| `pageCursor` | query | `string` | no | Cursor returned by a previous request to continue fetching documents. |
| `withHtmlContent` | query | `boolean` | no | Include html_content in each document. |
| `withRawSourceUrl` | query | `boolean` | no | Include raw_source_url in each document when available. |
| `location` | query | `string` | no | Reader document location: new, later, shortlist, archive, or feed. |
| `tag` | query | `string` | no | Reader tag key. Pass an empty value to find untagged documents. Send multiple values as a string. |
