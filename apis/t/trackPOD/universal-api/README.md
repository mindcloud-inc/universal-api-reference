# <img src="https://images.mindcloud.co/apps/icons/unnamed_1774299699382.png" alt="Track-POD logo" width="28" height="28"> Track-POD: Universal API

Last-mile delivery and electronic proof-of-delivery platform for managing orders, routes, drivers, vehicles, and delivery tracking.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/trackPOD/latest
- **Category:** Commerce / Supply Chain
- **Actions:** 31
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.track-pod.com/
- **Vendor API docs:** https://api.track-pod.com/index.html

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Test Authorization](actions/test-authorization.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/trackPOD/latest/actions/test-authorization?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (31)

### Authorization Check

| Action | Method | Description |
| --- | --- | --- |
| [Test Authorization](actions/test-authorization.md) | GET | Retrieves authorization and rate limit status from Track-POD. |

### Driver

| Action | Method | Description |
| --- | --- | --- |
| [Add Driver](actions/add-driver.md) | POST | Creates a new driver in Track-POD. |
| [Delete Driver By Id](actions/delete-driver-by-id.md) | DELETE | Deletes an existing driver from Track-POD by ID. |
| [Get Driver By Id](actions/get-driver-by-id.md) | GET | Retrieves a driver from Track-POD by ID. |
| [List Drivers](actions/list-drivers.md) | GET | Retrieves drivers from Track-POD. |
| [Update Driver](actions/update-driver.md) | PUT | Updates an existing driver in Track-POD. |

### Orders

| Action | Method | Description |
| --- | --- | --- |
| [Add Existing Order To Route](actions/add-existing-order-to-route.md) | PUT | Updates a Track-POD route by adding an existing order. |
| [Add Existing Order To Route By Code](actions/add-existing-order-to-route-by-code.md) | PUT | Updates a Track-POD route by adding an existing order by number. |
| [Add Unscheduled Order](actions/add-unscheduled-order.md) | POST | Creates a new unscheduled order in Track-POD. |
| [Add Unscheduled Orders Bulk](actions/add-unscheduled-orders-bulk.md) | POST | Creates new unscheduled orders in bulk in Track-POD. |
| [Delete Order By Id](actions/delete-order-by-id.md) | DELETE | Deletes an existing order from Track-POD by ID. |
| [Delete Order By Number](actions/delete-order-by-number.md) | DELETE | Deletes an existing order from Track-POD by number. |
| [Get Order By Id](actions/get-order-by-id.md) | GET | Retrieves an order from Track-POD by ID. |
| [Get Order By Number](actions/get-order-by-number.md) | GET | Retrieves an order from Track-POD by number. |
| [List Orders By Date](actions/list-orders-by-date.md) | GET | Retrieves orders from Track-POD by date. |
| [List Orders By Status Date](actions/list-orders-by-status-date.md) | GET | Retrieves orders from Track-POD by status date using UTC time. |
| [Update Order](actions/update-order.md) | PUT | Updates an existing order in Track-POD. |

### Reject Reason

| Action | Method | Description |
| --- | --- | --- |
| [List Reject Reasons](actions/list-reject-reasons.md) | GET | Retrieves reject reasons from Track-POD. |

### Route

| Action | Method | Description |
| --- | --- | --- |
| [Add Route](actions/add-route.md) | POST | Creates a new route in Track-POD. |
| [Delete Route By Code](actions/delete-route-by-code.md) | DELETE | Deletes an existing route from Track-POD by code. |
| [Delete Route By Id](actions/delete-route-by-id.md) | DELETE | Deletes an existing route from Track-POD by ID. |
| [Get Route By Code](actions/get-route-by-code.md) | GET | Retrieves a route from Track-POD by code. |
| [Get Route By Id](actions/get-route-by-id.md) | GET | Retrieves a route from Track-POD by ID. |
| [Get Route Track By Code](actions/get-route-track-by-code.md) | GET | Retrieves route tracking details from Track-POD by code. |
| [Get Route Track By Id](actions/get-route-track-by-id.md) | GET | Retrieves route tracking details from Track-POD by ID. |
| [List Routes By Date](actions/list-routes-by-date.md) | GET | Retrieves routes from Track-POD by date. |

### Vehicle

| Action | Method | Description |
| --- | --- | --- |
| [Add Vehicle](actions/add-vehicle.md) | POST | Creates a new vehicle in Track-POD. |
| [Delete Vehicle By Id](actions/delete-vehicle-by-id.md) | DELETE | Deletes an existing vehicle from Track-POD by ID. |
| [Get Vehicle By Id](actions/get-vehicle-by-id.md) | GET | Retrieves a vehicle from Track-POD by ID. |
| [List Vehicles](actions/list-vehicles.md) | GET | Retrieves vehicles from Track-POD. |
| [Update Vehicle](actions/update-vehicle.md) | PUT | Updates an existing vehicle in Track-POD. |

