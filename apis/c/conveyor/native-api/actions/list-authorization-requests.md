# List Authorization Requests with Conveyor

Retrieves authorization requests from Conveyor with optional filters.

## Endpoint

- **Method:** `GET`
- **Path:** `/v2/exchange/authorization_requests`
- **Base URL:** `https://api.conveyor.com/api`
- **Official documentation:** [List Authorization Requests](https://docs.conveyor.com/reference/get-authorization-requests)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `email` | query | `string` | no | Email address filter. |
| `status` | query | `string` | no | Authorization request status. |
