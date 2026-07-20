# Reposition Products with Big Cartel

Updates product positions in Big Cartel.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/v1/accounts/[:account-id]/relationships/products`
- **Base URL:** `https://api.bigcartel.com`
- **Official documentation:** [Reposition Products](https://developers.bigcartel.com/api/v1)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `account-id` | path | `number` | yes | The Big Cartel account ID. |
| `data[].id` | body | `number` | yes | — |
