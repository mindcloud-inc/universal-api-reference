# List Customers with Hiflow

Retrieves customers from Hiflow.

## Endpoint

- **Method:** `GET`
- **Path:** `/customer`
- **Base URL:** `https://{account}.hiflow.net/rest`
- **Official documentation:** [List Customers](https://www.hiflow.net/openapi/#tag/Customers/paths/~1customer/get)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `search` | query | `string` | no | Search string applied on the customer name field. |
| `include_coord` | query | `boolean` | no | Include GPS coordinates (lat/lng) for each customer. |
