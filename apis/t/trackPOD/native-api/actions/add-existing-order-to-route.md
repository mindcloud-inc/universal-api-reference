# Add Existing Order To Route with Track-POD

Updates a Track-POD route by adding an existing order.

## Endpoint

- **Method:** `PUT`
- **Path:** `/Route/Id/:id/Order/Id/:orderId`
- **Base URL:** `https://api.track-pod.com`
- **Official documentation:** [Add Existing Order To Route](https://api.track-pod.com/index.html#/Route/MoveOrderToRouteByIdById)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `allowReschedule` | query | `boolean` | no | Allow rescheduling and transferring an order with failed delivery status from another route. |
| `allowTransfer` | query | `boolean` | no | Allow transferring an order without delivery status from another route. |
| `id` | path | `string` | yes | Track-POD unique identifier for the route. |
| `orderId` | path | `string` | yes | Track-POD unique identifier for the order. |
