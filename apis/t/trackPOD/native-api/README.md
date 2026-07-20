# Track-POD: Native API Reference

A consolidated summary of Track-POD's API configuration and 31 documented operations, with links to official documentation.

- **Official docs:** https://api.track-pod.com/index.html
- **OpenAPI specification:** https://api.track-pod.com/swagger/v1/swagger.json
- **API base URL:** `https://api.track-pod.com`

## Authentication

### API Key

Track-POD uses an API key sent in the X-API-KEY request header.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
X-API-KEY: <apiKey>
```

[Official authentication documentation](https://www.track-pod.com/blog/track-pod-api-explained/)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Endpoints (31 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Add Driver](actions/add-driver.md) | `POST /Driver` | [docs](https://api.track-pod.com/index.html#/Driver/AddDriver) |
| [Add Existing Order To Route](actions/add-existing-order-to-route.md) | `PUT /Route/Id/:id/Order/Id/:orderId` | [docs](https://api.track-pod.com/index.html#/Route/MoveOrderToRouteByIdById) |
| [Add Existing Order To Route By Code](actions/add-existing-order-to-route-by-code.md) | `PUT /Route/Code/:code/Order/Number/:number` | [docs](https://api.track-pod.com/index.html#/Route/MoveOrderToRouteByCodeByNumber) |
| [Add Route](actions/add-route.md) | `POST /Route` | [docs](https://api.track-pod.com/index.html#/Route/AddRoute) |
| [Add Unscheduled Order](actions/add-unscheduled-order.md) | `POST /Order` | [docs](https://api.track-pod.com/index.html#/Order/AddOrder) |
| [Add Unscheduled Orders Bulk](actions/add-unscheduled-orders-bulk.md) | `POST /Order/Bulk` | [docs](https://api.track-pod.com/index.html#/Order/AddOrderBulk) |
| [Add Vehicle](actions/add-vehicle.md) | `POST /Vehicle` | [docs](https://api.track-pod.com/index.html#/Vehicle/AddVehicle) |
| [Delete Driver By Id](actions/delete-driver-by-id.md) | `DELETE /Driver/Id/:id` | [docs](https://api.track-pod.com/index.html#/Driver/DeleteDriverById) |
| [Delete Order By Id](actions/delete-order-by-id.md) | `DELETE /Order/Id/:id` | [docs](https://api.track-pod.com/index.html#/Order/DeleteOrderById) |
| [Delete Order By Number](actions/delete-order-by-number.md) | `DELETE /Order/Number/:number` | [docs](https://api.track-pod.com/index.html#/Order/DeleteOrderByNumber) |
| [Delete Route By Code](actions/delete-route-by-code.md) | `DELETE /Route/Code/:code` | [docs](https://api.track-pod.com/index.html#/Route/DeleteRouteByCode) |
| [Delete Route By Id](actions/delete-route-by-id.md) | `DELETE /Route/Id/:id` | [docs](https://api.track-pod.com/index.html#/Route/DeleteRouteById) |
| [Delete Vehicle By Id](actions/delete-vehicle-by-id.md) | `DELETE /Vehicle/:id` | [docs](https://api.track-pod.com/index.html#/Vehicle/DeleteVehicle) |
| [Get Driver By Id](actions/get-driver-by-id.md) | `GET /Driver/Id/:id` | [docs](https://api.track-pod.com/index.html#/Driver/GetDriverById) |
| [Get Order By Id](actions/get-order-by-id.md) | `GET /Order/Id/:id` | [docs](https://api.track-pod.com/index.html#/Order/GetOrderById) |
| [Get Order By Number](actions/get-order-by-number.md) | `GET /Order/Number/:number` | [docs](https://api.track-pod.com/index.html#/Order/GetOrderByNumber) |
| [Get Route By Code](actions/get-route-by-code.md) | `GET /Route/Code/:code` | [docs](https://api.track-pod.com/index.html#/Route/GetRouteByCode) |
| [Get Route By Id](actions/get-route-by-id.md) | `GET /Route/Id/:id` | [docs](https://api.track-pod.com/index.html#/Route/GetRouteById) |
| [Get Route Track By Code](actions/get-route-track-by-code.md) | `GET /Route/Track/Code/:code` | [docs](https://api.track-pod.com/index.html#/Route/GetRouteTrackByCode) |
| [Get Route Track By Id](actions/get-route-track-by-id.md) | `GET /Route/Track/Id/:id` | [docs](https://api.track-pod.com/index.html#/Route/GetRouteTrackById) |
| [Get Vehicle By Id](actions/get-vehicle-by-id.md) | `GET /Vehicle/:id` | [docs](https://api.track-pod.com/index.html#/Vehicle/GetVehicle) |
| [List Drivers](actions/list-drivers.md) | `GET /Driver` | [docs](https://api.track-pod.com/index.html#/Driver/GetDrivers) |
| [List Orders By Date](actions/list-orders-by-date.md) | `GET /Order/Date/:date` | [docs](https://api.track-pod.com/index.html#/Order/GetOrderByDate) |
| [List Orders By Status Date](actions/list-orders-by-status-date.md) | `GET /Order/Status/Date/:date` | [docs](https://api.track-pod.com/index.html#/Order/GetOrderByStatusDate) |
| [List Reject Reasons](actions/list-reject-reasons.md) | `GET /RejectReason` | [docs](https://api.track-pod.com/index.html#/RejectReason/GetRejectReasonsList) |
| [List Routes By Date](actions/list-routes-by-date.md) | `GET /Route/Date/:date` | [docs](https://api.track-pod.com/index.html#/Route/GetRouteByDate) |
| [List Vehicles](actions/list-vehicles.md) | `GET /Vehicle` | [docs](https://api.track-pod.com/index.html#/Vehicle/GetVehicles) |
| [Test Authorization](actions/test-authorization.md) | `GET /Test` | [docs](https://api.track-pod.com/index.html#/Test/Test) |
| [Update Driver](actions/update-driver.md) | `PUT /Driver` | [docs](https://api.track-pod.com/index.html#/Driver/UpdateDriver) |
| [Update Order](actions/update-order.md) | `PUT /Order` | [docs](https://api.track-pod.com/index.html#/Order/UpdateOrder) |
| [Update Vehicle](actions/update-vehicle.md) | `PUT /Vehicle` | [docs](https://api.track-pod.com/index.html#/Vehicle/UpdateVehicle) |
