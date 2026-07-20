# Update Category with Big Cartel

Updates an existing category in Big Cartel.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/v1/accounts/[:account-id]/categories/[:category-id]`
- **Base URL:** `https://api.bigcartel.com`
- **Official documentation:** [Update Category](https://developers.bigcartel.com/api/v1)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `account-id` | path | `number` | yes | The Big Cartel account ID. |
| `category-id` | path | `string` | yes | Category identifier from the categories endpoint. |
| `data.id` | body | `string` | yes | — |
| `data.attributes.name` | body | `string` | yes | — |
