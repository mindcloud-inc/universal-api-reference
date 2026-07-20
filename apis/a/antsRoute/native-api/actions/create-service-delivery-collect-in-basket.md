# Create Service/Delivery/Collect in Basket with AntsRoute

Creates a new basket order in AntsRoute.

## Endpoint

- **Method:** `POST`
- **Path:** `/capi/order/basket`
- **Base URL:** `https://app.antsroute.com`
- **Official documentation:** [Create Service/Delivery/Collect in Basket](https://app.antsroute.com/doc-api/index.html#/Service%2FDelivery%2FCollect/createBasketOrder)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `customer.address` | body | `string` | yes | Customer address. |
| `customer.firstName` | body | `string` | no | Customer first name. |
| `customer.id` | body | `number` | no | Existing customer identifier. |
| `customer.lastName` | body | `string` | yes | Customer last name. |
| `customer.latitude` | body | `number` | yes | Customer latitude. |
| `customer.longitude` | body | `number` | yes | Customer longitude. |
| `dueDate` | body | `string` | yes | Order due date in `yyyy-MM-dd` format. |
| `duration` | body | `number` | yes | Planned service duration in minutes. |
| `externalId` | body | `string` | no | Unique external order identifier. |
| `openDate` | body | `string` | yes | Order open date in `yyyy-MM-dd` format. |
| `type` | body | `string` | yes | Order type, for example SERVICE. |
