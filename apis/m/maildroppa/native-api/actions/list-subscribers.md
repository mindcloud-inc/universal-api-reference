# List Subscribers with Maildroppa

Retrieves subscribers from Maildroppa with pagination.

## Endpoint

- **Method:** `GET`
- **Path:** `/subscribers`
- **Base URL:** `https://api.maildroppa.com`
- **Official documentation:** [List Subscribers](https://api.maildroppa.com)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `pageNumber` | query | `number` | no | Page number. |
| `pageSize` | query | `number` | no | Number of items per page. |
| `query` | query | `string` | no | Free-text search query. |
| `status` | query | `string` | no | Subscriber status filter. |
