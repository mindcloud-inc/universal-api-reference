# List Webhook Endpoints with Chainstream

Retrieves webhook endpoints from Chainstream.

## Endpoint

- **Method:** `GET`
- **Path:** `/v2/webhook/endpoint`
- **Base URL:** `https://api.chainstream.io`
- **Official documentation:** [List Webhook Endpoints](https://docs.chainstream.io/en/api-reference/endpoint/data/webhook/v2/webhook-endpoint-get)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `limit` | query | `number` | no | Number of results per page |
| `iterator` | query | `string` | no | Pagination iterator |
| `order` | query | `string` | no | Ordering direction for paginated endpoint listing |
