# List API Keys with Documo

Retrieves API key records from Documo.

## Endpoint

- **Method:** `GET`
- **Path:** `/api-keys`
- **Base URL:** `https://api.documo.com`
- **Official documentation:** [List API Keys](https://docs.documo.com/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `userId` | query | `string` | no | User UUID to filter API keys by owner. |
| `accountId` | query | `string` | no | Account UUID to filter API keys. |
| `search` | query | `string` | no | Keyword to search in the API key name. |
| `limit` | query | `number` | no | Number of results per page. Default 20, max 100. |
| `page` | query | `number` | no | Results page number. Default 1. |
| `status` | query | `string` | no | Filter API keys by status. Possible values: active, expired. |
