# <img src="https://images.mindcloud.co/apps/icons/smart-routes_1774456975779.png" alt="SmartRoutes logo" width="28" height="28"> SmartRoutes: Universal API

Plan routes, dispatch drivers, track deliveries, and capture proof

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/smartRoutes/latest
- **Category:** Commerce / Supply Chain
- **Actions:** 22
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://smartroutes.io/
- **Vendor API docs:** https://api.smartroutes.io/v2/docs/api/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Customers](actions/list-customers.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/smartRoutes/latest/actions/list-customers?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (22)

### Booking Availability

| Action | Method | Description |
| --- | --- | --- |
| [Check Booking Availability](actions/check-booking-availability.md) | GET |  |

### Capacity

| Action | Method | Description |
| --- | --- | --- |
| [List Capacities](actions/list-capacities.md) | GET |  |

### Custom Field

| Action | Method | Description |
| --- | --- | --- |
| [List Custom Fields](actions/list-custom-fields.md) | GET |  |

### Customer

| Action | Method | Description |
| --- | --- | --- |
| [Get Customer](actions/get-customer.md) | GET |  |
| [List Customers](actions/list-customers.md) | GET |  |
| [Update Customer](actions/update-customer.md) | PUT |  |

### Notification Task

| Action | Method | Description |
| --- | --- | --- |
| [List Notification Tasks](actions/list-notification-tasks.md) | GET |  |

### Notification Template

| Action | Method | Description |
| --- | --- | --- |
| [List Notification Templates](actions/list-notification-templates.md) | GET |  |

### Order

| Action | Method | Description |
| --- | --- | --- |
| [Delete Order By Number](actions/delete-order-by-number.md) | DELETE |  |
| [Get Order](actions/get-order.md) | GET |  |
| [List Orders](actions/list-orders.md) | GET |  |
| [Update Order](actions/update-order.md) | PUT |  |

### Plan

| Action | Method | Description |
| --- | --- | --- |
| [Get Plan](actions/get-plan.md) | GET |  |
| [List Plans](actions/list-plans.md) | GET |  |

### Route

| Action | Method | Description |
| --- | --- | --- |
| [List Routes](actions/list-routes.md) | GET |  |

### Third Party

| Action | Method | Description |
| --- | --- | --- |
| [List Third Parties](actions/list-third-parties.md) | GET |  |

### Vehicle

| Action | Method | Description |
| --- | --- | --- |
| [Create Vehicle](actions/create-vehicle.md) | POST |  |
| [Delete Vehicle](actions/delete-vehicle.md) | DELETE |  |
| [Get Vehicle](actions/get-vehicle.md) | GET |  |
| [List Vehicles](actions/list-vehicles.md) | GET |  |
| [Update Vehicle](actions/update-vehicle.md) | PUT |  |

### Zone Group

| Action | Method | Description |
| --- | --- | --- |
| [List Zone Groups](actions/list-zone-groups.md) | GET |  |

