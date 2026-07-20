# List Subscribers with Sequenzy

Retrieves a paginated list of subscribers from Sequenzy.

## Endpoint

- **Method:** `GET`
- **Path:** `/subscribers`
- **Base URL:** `https://api.sequenzy.com/api/v1`
- **Official documentation:** [List Subscribers](https://docs.sequenzy.com/api-reference/subscribers/list)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `email` | query | `string` | no | Filter by partial email match. |
| `limit` | query | `string` | no | Items per page. Max 100. |
| `page` | query | `string` | no | Page number. |
| `status` | query | `string` | no | Filter by subscriber status. |
