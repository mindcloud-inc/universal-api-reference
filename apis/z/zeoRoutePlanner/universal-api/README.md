# <img src="https://images.mindcloud.co/apps/icons/cropped-logo192-192x192_1774460696165.png" alt="Zeo Route Planner logo" width="28" height="28"> Zeo Route Planner: Universal API

Route planning and fleet operations platform for managing drivers, stops, routes, pickup and delivery routes, and real-time webhook events.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/zeoRoutePlanner/latest
- **Category:** Support / Field Service
- **Actions:** 13
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://zeorouteplanner.com
- **Vendor API docs:** https://api.zeorouteplanner.com/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Drivers](actions/list-drivers.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/zeoRoutePlanner/latest/actions/list-drivers?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (13)

### Driver

| Action | Method | Description |
| --- | --- | --- |
| [Create Driver](actions/create-driver.md) | POST | Creates a new driver in Zeo Route Planner. |
| [Delete Driver](actions/delete-driver.md) | DELETE | Deletes an existing driver from Zeo Route Planner. |
| [List Drivers](actions/list-drivers.md) | GET | Retrieves drivers from Zeo Route Planner. |

### Route

| Action | Method | Description |
| --- | --- | --- |
| [Create Pickup Delivery Route](actions/create-pickup-delivery-route.md) | POST | Creates a pickup delivery route in Zeo Route Planner. |
| [Create Route](actions/create-route.md) | POST | Creates a new route in Zeo Route Planner. |
| [Delete Pickup Delivery Route](actions/delete-pickup-delivery-route.md) | DELETE | Deletes a pickup delivery route from Zeo Route Planner. |
| [Delete Route](actions/delete-route.md) | DELETE | Deletes an existing route from Zeo Route Planner. |
| [Get Pickup Delivery Route Info](actions/get-pickup-delivery-route-info.md) | GET | Retrieves pickup delivery route details from Zeo Route Planner. |
| [Get Pickup Delivery Route Optimized Info](actions/get-pickup-delivery-route-optimized-info.md) | GET | Retrieves optimized pickup delivery route details from Zeo Route Planner. |
| [Get Route Info](actions/get-route-info.md) | GET | Retrieves route details from Zeo Route Planner. |
| [Get Route Optimized Info](actions/get-route-optimized-info.md) | GET | Retrieves optimized route details from Zeo Route Planner. |
| [List Driver Routes](actions/list-driver-routes.md) | GET | Retrieves routes for a driver in Zeo Route Planner. |

### Stop

| Action | Method | Description |
| --- | --- | --- |
| [Create Stops](actions/create-stops.md) | POST | Creates stops in Zeo Route Planner. |

