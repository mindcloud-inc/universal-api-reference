# Get landing pages with Maildrip

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v1/get-all-pages`
- **Base URL:** `https://api.maildrip.io`
- **Official documentation:** [Get landing pages](https://api.maildrip.io/docs/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `search` | query | `string` | no | Search term to filter landing pages by title |
| `limit` | query | `string` | no | Number of items per page or "all" to retrieve all pages |
| `page` | query | `number` | no | Page number for pagination |
