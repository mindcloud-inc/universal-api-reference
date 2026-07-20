# Search Documents with Zoho Writer

Finds documents in Zoho Writer.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/documents/search`
- **Base URL:** `{api_domain}/writer/api`
- **Official documentation:** [Search Documents](https://www.zoho.com/writer/help/api/v1/search-document.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `query` | query | `string` | yes | Search term for documents. |
| `limit` | query | `number` | no | Maximum number of matching documents to return. |
| `offset` | query | `number` | no | Zero-based offset for paginating search results. |
| `team_id` | query | `string` | no | Optional WorkDrive team ID to search within a specific team. |
