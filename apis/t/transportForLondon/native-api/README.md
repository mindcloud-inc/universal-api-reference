# Transport for London: Native API Reference

A consolidated summary of Transport for London's API configuration and 23 documented operations, with links to official documentation.

- **Official docs:** https://api.tfl.gov.uk/swagger/ui/index.html
- **OpenAPI specification:** https://api.tfl.gov.uk/swagger/docs/v1
- **API base URL:** `https://api.tfl.gov.uk`

## Authentication

### API Key

TfL Unified API key used as the app_key query parameter for higher request limits.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://api-portal.tfl.gov.uk/)

## API conventions

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |

Responses from this API use JSON.

## Retry behavior

Retry responses with status codes `429,500,502,503,504`. Wait 1000 ms before the first retry. Stop after 2 attempts. Multiply the delay by 2 after each failed attempt.

## Endpoints (23 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Get Bike Point](actions/bike-point.md) | `GET /BikePoint/:id` | [docs](https://api.tfl.gov.uk/swagger/ui/index.html#!/BikePoint/BikePoint_Get) |
| [List Bike Points](actions/bike-points.md) | `GET /BikePoint` | [docs](https://api.tfl.gov.uk/swagger/ui/index.html#!/BikePoint/BikePoint_GetAll) |
| [List Journey Modes](actions/journey-modes.md) | `GET /Journey/Meta/Modes` | [docs](https://api.tfl.gov.uk/swagger/ui/index.html#!/Journey/Journey_Meta) |
| [Get Line Arrivals At Stop](actions/line-arrivals-at-stop.md) | `GET /Line/:ids/Arrivals/:stopPointId` | [docs](https://api.tfl.gov.uk/swagger/ui/index.html#!/Line/Line_Arrivals) |
| [Get Line Disruptions](actions/line-disruptions.md) | `GET /Line/:ids/Disruption` | [docs](https://api.tfl.gov.uk/swagger/ui/index.html#!/Line/Line_Disruption) |
| [Get Line Route Sequence](actions/line-route-sequence.md) | `GET /Line/:id/Route/Sequence/:direction` | [docs](https://api.tfl.gov.uk/swagger/ui/index.html#!/Line/Line_RouteSequence) |
| [Get Line Status By IDs](actions/line-status-by-ids.md) | `GET /Line/:ids/Status` | [docs](https://api.tfl.gov.uk/swagger/ui/index.html#!/Line/Line_StatusByIds) |
| [Get Line Status By Mode](actions/line-status-by-mode.md) | `GET /Line/Mode/:modes/Status` | [docs](https://api.tfl.gov.uk/swagger/ui/index.html#!/Line/Line_StatusByMode) |
| [List Line Stop Points](actions/line-stop-points.md) | `GET /Line/:id/StopPoints` | [docs](https://api.tfl.gov.uk/swagger/ui/index.html#!/Line/Line_StopPoints) |
| [Get Lines By Mode](actions/lines-by-mode.md) | `GET /Line/Mode/:modes` | [docs](https://api.tfl.gov.uk/swagger/ui/index.html#!/Line/Line_GetByMode) |
| [List Line Routes](actions/list-line-routes.md) | `GET /Line/Route` | [docs](https://api.tfl.gov.uk/swagger/ui/index.html#!/Line/Line_Route) |
| [Find Nearby Stop Points](actions/nearby-stop-points.md) | `GET /StopPoint` | [docs](https://api.tfl.gov.uk/swagger/ui/index.html#!/StopPoint/StopPoint_GetByGeoPoint) |
| [Plan Journey](actions/plan-journey.md) | `GET /Journey/JourneyResults/:from/to/:to` | [docs](https://api.tfl.gov.uk/swagger/ui/index.html#!/Journey/Journey_JourneyResults) |
| [Get Road Disruptions](actions/road-disruptions.md) | `GET /Road/:ids/Disruption` | [docs](https://api.tfl.gov.uk/swagger/ui/index.html#!/Road/Road_Disruption) |
| [Get Road Status](actions/road-status.md) | `GET /Road/:ids/Status` | [docs](https://api.tfl.gov.uk/swagger/ui/index.html#!/Road/Road_Status) |
| [List Roads](actions/roads.md) | `GET /Road` | [docs](https://api.tfl.gov.uk/swagger/ui/index.html#!/Road/Road_Get) |
| [Search Bike Points](actions/search-bike-points.md) | `GET /BikePoint/Search` | [docs](https://api.tfl.gov.uk/swagger/ui/index.html#!/BikePoint/BikePoint_Search) |
| [Search Lines](actions/search-lines.md) | `GET /Line/Search/:query` | [docs](https://api.tfl.gov.uk/swagger/ui/index.html#!/Line/Line_Search) |
| [Search Stop Points](actions/search-stop-points.md) | `GET /StopPoint/Search/:query` | [docs](https://api.tfl.gov.uk/swagger/ui/index.html#!/StopPoint/StopPoint_Search) |
| [Search TfL](actions/search-tfl.md) | `GET /Search` | [docs](https://api.tfl.gov.uk/swagger/ui/index.html#!/Search/Search_Get) |
| [Get Stop Arrivals](actions/stop-arrivals.md) | `GET /StopPoint/:id/Arrivals` | [docs](https://api.tfl.gov.uk/swagger/ui/index.html#!/StopPoint/StopPoint_Arrivals) |
| [Get Stop Points By IDs](actions/stop-points-by-ids.md) | `GET /StopPoint/:ids` | [docs](https://api.tfl.gov.uk/swagger/ui/index.html#!/StopPoint/StopPoint_Get) |
| [Get Stop Points By Mode](actions/stop-points-by-mode.md) | `GET /StopPoint/Mode/:modes` | [docs](https://api.tfl.gov.uk/swagger/ui/index.html#!/StopPoint/StopPoint_GetByMode) |
