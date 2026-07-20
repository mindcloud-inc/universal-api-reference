# <img src="https://images.mindcloud.co/apps/icons/caltrain_1776356785432.png" alt="Caltrain logo" width="28" height="28"> Caltrain: Universal API

Track Caltrain routes, stops, service alerts, and live train data

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/caltrain/latest
- **Category:** Productivity / Scheduling
- **Actions:** 12
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.caltrain.com
- **Vendor API docs:** https://www.caltrain.com/developer-resources

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Stop Alerts](actions/get-stop-alerts.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/caltrain/latest/actions/get-stop-alerts?connectionId=$CONNECTION_ID&stopId=22nd_street" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (12)

### Alerts

| Action | Method | Description |
| --- | --- | --- |
| [Get Stop Alerts](actions/get-stop-alerts.md) | GET | Retrieves alerts for a Caltrain stop. |
| [List Node Service Alerts](actions/list-node-service-alerts.md) | GET | Retrieves service alerts for a Caltrain node. |
| [List Service Alerts](actions/list-service-alerts.md) | GET | Retrieves Caltrain service alerts. |

### Amenity

| Action | Method | Description |
| --- | --- | --- |
| [List Stop Amenities](actions/list-stop-amenities.md) | GET | Retrieves amenities for a Caltrain stop. |
| [Search Amenities](actions/search-amenities.md) | GET | Finds Caltrain amenities within map bounds. |

### Locations

| Action | Method | Description |
| --- | --- | --- |
| [Search Locations](actions/search-locations.md) | GET | Finds Caltrain locations by search query. |

### Route

| Action | Method | Description |
| --- | --- | --- |
| [List Routes](actions/list-routes.md) | GET | Retrieves Caltrain routes. |

### Schedules

| Action | Method | Description |
| --- | --- | --- |
| [Get Stop Predictions](actions/get-stop-predictions.md) | GET | Retrieves arrival predictions for a Caltrain stop. |
| [Get Trip Updates Feed](actions/list-trip-updates.md) | GET | Retrieves the Caltrain trip updates feed. |

### Stop

| Action | Method | Description |
| --- | --- | --- |
| [List Nearby Stops](actions/list-nearby-stops.md) | GET | Finds Caltrain stops near a location. |
| [List Route Stops](actions/list-route-stops.md) | GET | Retrieves stops for a Caltrain route. |

### Vehicle Position

| Action | Method | Description |
| --- | --- | --- |
| [Get Vehicle Positions Feed](actions/list-vehicle-positions.md) | GET | Retrieves the Caltrain vehicle positions feed. |

