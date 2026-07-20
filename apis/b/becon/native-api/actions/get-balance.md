# Get Balance with Becon

Retrieves BTC wallet balances from Becon by address.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/user/balance`
- **Base URL:** `https://external-api.bcon.global/api`
- **Official documentation:** [Get Balance](https://bcon.global/integrations/api/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `address` | query | `string` | yes | Whitespace-separated wallet addresses to inspect. |
