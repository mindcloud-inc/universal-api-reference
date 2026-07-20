# Create Category with Big Cartel

Creates a category in Big Cartel.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/accounts/[:account-id]/categories`
- **Base URL:** `https://api.bigcartel.com`
- **Official documentation:** [Create Category](https://developers.bigcartel.com/api/v1)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `account-id` | path | `number` | yes | The Big Cartel account ID. |
| `id` | body | `string` | no | — |
| `data.attributes.name` | body | `string` | yes | — |
