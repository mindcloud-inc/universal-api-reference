# Get All Customers with BigCommerce

## Endpoint

- **Method:** `GET`
- **Path:** `/v3/customers`
- **Base URL:** `https://api.bigcommerce.com/stores/{storeHash}`
- **Official documentation:** [Get All Customers](https://developer.bigcommerce.com/docs/rest-management/customers#get-all-customers)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id:in` | query | `string` | no | Get a specific customer by their ID Send multiple values as a string. |
| `name:in` | query | `string` | no | Filter items by first_name and last_name. name=james moriarty Type: array[string] Send multiple values as a array. |
| `email:in` | query | `string` | no | Filter items by email. email:in=janedoe@example.com Send multiple values as a array. |
| `date_modified:min` | query | `string` | no | Filter items by minimum date modified, for example, 2024-05-14T09:34:00 or 2024-05-14. Returns customers modified after this date. |
| `company:in` | query | `string` | no | Send multiple values as a array. |
| `name:like` | query | `string` | no | Send multiple values as a array. |
| `phone:in` | query | `string` | no | — |
