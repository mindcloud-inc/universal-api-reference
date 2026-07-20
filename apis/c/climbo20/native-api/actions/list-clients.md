# List Clients with Climbo 2.0

Retrieves agency clients from Climbo 2.0.

## Endpoint

- **Method:** `GET`
- **Path:** `/clients`
- **Base URL:** `https://api.climbo.com`
- **Official documentation:** [List Clients](https://climbo.readme.io/reference/list-clients)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `page` | query | `number` | no | If not set returns the first page. |
| `plan_id` | query | `string` | no | Filter by plan ID. |
| `status` | query | `string` | no | Filter by customer status. |
| `email` | query | `string` | no | Filter by customer email. |
