# Reposition Categories with Big Cartel

Updates category positions in Big Cartel.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/v1/accounts/[:account-id]/relationships/categories`
- **Base URL:** `https://api.bigcartel.com`
- **Official documentation:** [Reposition Categories](https://developers.bigcartel.com/api/v1)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `account-id` | path | `number` | yes | The Big Cartel account ID. |
| `data[].id` | body | `string` | yes | — |
