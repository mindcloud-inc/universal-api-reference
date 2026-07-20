# Get your account transactions with Routee

Retrieves your current Routee account transactions.

## Endpoint

- **Method:** `GET`
- **Path:** `/accounts/me/transactions`
- **Base URL:** `https://connect.routee.net`
- **Official documentation:** [Get your account transactions](https://docs.routee.net/reference/transactions)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `from` | query | `date` | yes | [ISO-8601](https://en.wikipedia.org/wiki/ISO_8601) date-time format |
| `to` | query | `date` | yes | [ISO-8601](https://en.wikipedia.org/wiki/ISO_8601) date-time format |
| `page` | query | `number` | no | The page number to retrieve, default value is 0 (meaning the first page). |
| `size` | query | `number` | no | The number of items to retrieve |
