# List Transaction History with Becon

Retrieves BTC transaction history from Becon by address.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/user/history`
- **Base URL:** `https://external-api.bcon.global/api`
- **Official documentation:** [List Transaction History](https://bcon.global/integrations/api/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `address` | query | `string` | yes | Whitespace-separated wallet addresses to inspect. |
| `page` | query | `string` | no | Page number for paginated transaction history. |
