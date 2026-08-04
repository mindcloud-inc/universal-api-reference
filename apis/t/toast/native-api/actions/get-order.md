# Get Order with Toast

Retrieves one order by its Toast GUID.

## Endpoint

- **Method:** `GET`
- **Path:** `/orders/v2/orders/:guid`
- **Base URL:** `{connection}`
- **API:** Orders
- **Official documentation:** [Get Order](https://doc.toasttab.com/openapi/orders/operation/ordersGuidGet/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `guid` | path | `string` | yes | The Toast GUID of the order to retrieve. |
