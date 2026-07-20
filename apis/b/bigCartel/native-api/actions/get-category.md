# Get Category with Big Cartel

Retrieves a category from Big Cartel.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/accounts/[:account-id]/categories/[:category-id]`
- **Base URL:** `https://api.bigcartel.com`
- **Official documentation:** [Get Category](https://developers.bigcartel.com/api/v1)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `account-id` | path | `number` | yes | The Big Cartel account ID. |
| `category-id` | path | `string` | yes | Category identifier from the categories endpoint. |
