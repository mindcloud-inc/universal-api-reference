# Caltrain: Native API Reference

A consolidated summary of Caltrain's API configuration and 12 documented operations, with links to official documentation.

- **Official docs:** https://www.caltrain.com/developer-resources
- **API base URL:** `https://www.caltrain.com`

## Authentication

### No authentication

Public Caltrain GTFS endpoints do not require credentials.

This API does not require request authentication.

[Official authentication documentation](https://www.caltrain.com/developer-resources)

## Endpoints (12 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Get Stop Alerts](actions/get-stop-alerts.md) | `GET /gtfs/stops/:stopId/alerts` | [docs](https://www.caltrain.com/developer-resources) |
| [Get Stop Predictions](actions/get-stop-predictions.md) | `GET /gtfs/stops/:stopId/predictions` | [docs](https://www.caltrain.com/developer-resources) |
| [List Nearby Stops](actions/list-nearby-stops.md) | `GET /gtfs/stops/nearby/:longitude/:latitude/:radius` | [docs](https://www.caltrain.com/developer-resources) |
| [List Node Service Alerts](actions/list-node-service-alerts.md) | `GET /gtfs/api/v1/servicealerts/:nodeId` | [docs](https://www.caltrain.com/developer-resources) |
| [List Route Stops](actions/list-route-stops.md) | `GET /gtfs/routes/:routeId/stops` | [docs](https://www.caltrain.com/developer-resources) |
| [List Routes](actions/list-routes.md) | `GET /gtfs/routes/all` | [docs](https://www.caltrain.com/developer-resources) |
| [List Service Alerts](actions/list-service-alerts.md) | `GET /gtfs/api/v1/servicealerts/Caltrain` | [docs](https://www.caltrain.com/developer-resources) |
| [List Stop Amenities](actions/list-stop-amenities.md) | `GET /gtfs/stops/:stopId/amenities` | [docs](https://www.caltrain.com/developer-resources) |
| [Get Trip Updates Feed](actions/list-trip-updates.md) | `GET /files/rt/tripupdates/CT.json` | [docs](https://www.caltrain.com/developer-resources) |
| [Get Vehicle Positions Feed](actions/list-vehicle-positions.md) | `GET /files/rt/vehiclepositions/CT.json` | [docs](https://www.caltrain.com/developer-resources) |
| [Search Amenities](actions/search-amenities.md) | `GET /search/amenities/:west,:south,:east,:north` | [docs](https://www.caltrain.com/developer-resources) |
| [Search Locations](actions/search-locations.md) | `GET /search/location_autocomplete` | [docs](https://www.caltrain.com/developer-resources) |
