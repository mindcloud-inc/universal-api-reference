# List Organization Orders with Eventbrite

Retrieves organization orders from Eventbrite.

## Endpoint

- **Method:** `GET`
- **Path:** `/organizations/:organizationId/orders/`
- **Base URL:** `https://www.eventbriteapi.com/v3`
- **Official documentation:** [List Organization Orders](https://www.eventbrite.com/platform/api#/reference/order/organization-orders/list-orders-by-organization)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `organizationId` | path | `string` | yes | Organization identifier. |
