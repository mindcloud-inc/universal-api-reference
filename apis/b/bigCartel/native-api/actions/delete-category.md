# Delete Category with Big Cartel

Deletes a category from Big Cartel.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/v1/accounts/[:account-id]/categories/[:category-id]`
- **Base URL:** `https://api.bigcartel.com`
- **Official documentation:** [Delete Category](https://developers.bigcartel.com/api/v1)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `account-id` | path | `number` | yes | The Big Cartel account ID. |
| `category-id` | path | `string` | yes | Category identifier from the categories endpoint. |
