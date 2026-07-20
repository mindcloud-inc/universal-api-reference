# List Conversations with Crisp

Retrieves conversations from Crisp.

## Endpoint

- **Method:** `GET`
- **Path:** `/website/:website_id/conversations/:page_number`
- **Base URL:** `https://api.crisp.chat/v1`
- **Official documentation:** [List Conversations](https://docs.crisp.chat/references/rest-api/v1/#list-conversations)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `website_id` | path | `string` | yes | The website identifier. |
| `page_number` | path | `number` | no | Page number for conversations paging. |
| `per_page` | query | `number` | no | Page size for conversations paging (between 20 and 50, defaults to 20). |
| `search_query` | query | `string` | no | Search query in conversations. |
