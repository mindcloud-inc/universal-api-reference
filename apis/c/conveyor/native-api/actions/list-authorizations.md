# List Authorizations with Conveyor

Retrieves authorizations from Conveyor with optional filters.

## Endpoint

- **Method:** `GET`
- **Path:** `/v2/exchange/authorizations`
- **Base URL:** `https://api.conveyor.com/api`
- **Official documentation:** [List Authorizations](https://docs.conveyor.com/reference/get-authorizations)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `email` | query | `string` | no | Email address filter. |
| `status` | query | `string` | no | Authorization status filter. |
