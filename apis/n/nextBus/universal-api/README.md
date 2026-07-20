# <img src="https://images.mindcloud.co/apps/icons/next-bus_1777307496501.png" alt="NextBus logo" width="28" height="28"> NextBus: Universal API

Access public transit agencies, routes, stops, and predictions

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/nextBus/latest
- **Actions:** 14
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://webservices.nextbus.com/
- **Vendor API docs:** https://retro.umoiq.com/xmlFeedDocs/NextBusXMLFeed.pdf

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Agencies](actions/list-agencies.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/nextBus/latest/actions/list-agencies?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (14)

### Agency

| Action | Method | Description |
| --- | --- | --- |
| [List Agencies](actions/list-agencies.md) | GET | Retrieves transit agencies from NextBus. |

### Message

| Action | Method | Description |
| --- | --- | --- |
| [List Active Messages](actions/list-active-messages.md) | GET | Retrieves active messages from NextBus. |
| [List Active Messages For Route](actions/list-active-messages-for-route.md) | GET | Retrieves active route messages from NextBus. |

### Prediction

| Action | Method | Description |
| --- | --- | --- |
| [Get Predictions By Route And Stop](actions/get-predictions-by-route-and-stop.md) | GET | Retrieves stop predictions from NextBus by route and stop. |
| [Get Predictions By Stop ID](actions/get-predictions-by-stop-id.md) | GET | Retrieves stop predictions from NextBus by stop ID. |
| [Get Predictions By Stop ID And Route](actions/get-predictions-by-stop-id-and-route.md) | GET | Retrieves stop predictions from NextBus by stop ID and route. |
| [Get Predictions For Multiple Stops](actions/get-predictions-for-multiple-stops.md) | GET | Retrieves stop predictions from NextBus for multiple stops. |

### Route

| Action | Method | Description |
| --- | --- | --- |
| [List Routes](actions/list-routes.md) | GET | Retrieves routes for an agency from NextBus. |

### Route Configuration

| Action | Method | Description |
| --- | --- | --- |
| [Get Route Config](actions/get-route-config.md) | GET | Retrieves a route configuration from NextBus. |
| [List Route Configs](actions/list-route-configs.md) | GET | Retrieves route configurations from NextBus. |

### Schedule

| Action | Method | Description |
| --- | --- | --- |
| [Get Route Schedule](actions/get-route-schedule.md) | GET | Retrieves a route schedule from NextBus. |

### Vehicle Location

| Action | Method | Description |
| --- | --- | --- |
| [Get Recent Vehicle Locations](actions/get-recent-vehicle-locations.md) | GET | Retrieves recent vehicle locations from NextBus. |
| [Get Vehicle Location](actions/get-vehicle-location.md) | GET | Retrieves a vehicle location from NextBus. |
| [List Vehicle Locations](actions/list-vehicle-locations.md) | GET | Retrieves changed vehicle locations from NextBus. |

