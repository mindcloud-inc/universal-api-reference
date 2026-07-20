# NextBus: Native API Reference

A consolidated summary of NextBus's API configuration and 14 documented operations, with links to official documentation.

- **Official docs:** https://retro.umoiq.com/xmlFeedDocs/NextBusXMLFeed.pdf
- **API base URL:** `https://retro.umoiq.com/service`

## Authentication

### No authentication

NextBus/Umo IQ public XML feed requests require no authentication.

This API does not require request authentication.

[Official authentication documentation](https://retro.umoiq.com/xmlFeedDocs/NextBusXMLFeed.pdf)

## API conventions

Responses from this API use XML.

## Endpoints (14 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Get Predictions By Route And Stop](actions/get-predictions-by-route-and-stop.md) | `GET /publicXMLFeed` | [docs](https://retro.umoiq.com/xmlFeedDocs/NextBusXMLFeed.pdf#page=14) |
| [Get Predictions By Stop ID](actions/get-predictions-by-stop-id.md) | `GET /publicXMLFeed` | [docs](https://retro.umoiq.com/xmlFeedDocs/NextBusXMLFeed.pdf#page=14) |
| [Get Predictions By Stop ID And Route](actions/get-predictions-by-stop-id-and-route.md) | `GET /publicXMLFeed` | [docs](https://retro.umoiq.com/xmlFeedDocs/NextBusXMLFeed.pdf#page=14) |
| [Get Predictions For Multiple Stops](actions/get-predictions-for-multiple-stops.md) | `GET /publicXMLFeed` | [docs](https://retro.umoiq.com/xmlFeedDocs/NextBusXMLFeed.pdf#page=15) |
| [Get Recent Vehicle Locations](actions/get-recent-vehicle-locations.md) | `GET /publicXMLFeed` | [docs](https://retro.umoiq.com/xmlFeedDocs/NextBusXMLFeed.pdf#page=20) |
| [Get Route Config](actions/get-route-config.md) | `GET /publicXMLFeed` | [docs](https://retro.umoiq.com/xmlFeedDocs/NextBusXMLFeed.pdf#page=8) |
| [Get Route Schedule](actions/get-route-schedule.md) | `GET /publicXMLFeed` | [docs](https://retro.umoiq.com/xmlFeedDocs/NextBusXMLFeed.pdf#page=16) |
| [Get Vehicle Location](actions/get-vehicle-location.md) | `GET /publicXMLFeed` | [docs](https://retro.umoiq.com/xmlFeedDocs/NextBusXMLFeed.pdf#page=21) |
| [List Active Messages](actions/list-active-messages.md) | `GET /publicXMLFeed` | [docs](https://retro.umoiq.com/xmlFeedDocs/NextBusXMLFeed.pdf#page=18) |
| [List Active Messages For Route](actions/list-active-messages-for-route.md) | `GET /publicXMLFeed` | [docs](https://retro.umoiq.com/xmlFeedDocs/NextBusXMLFeed.pdf#page=18) |
| [List Agencies](actions/list-agencies.md) | `GET /publicXMLFeed` | [docs](https://retro.umoiq.com/xmlFeedDocs/NextBusXMLFeed.pdf) |
| [List Route Configs](actions/list-route-configs.md) | `GET /publicXMLFeed` | [docs](https://retro.umoiq.com/xmlFeedDocs/NextBusXMLFeed.pdf#page=8) |
| [List Routes](actions/list-routes.md) | `GET /publicXMLFeed` | [docs](https://retro.umoiq.com/xmlFeedDocs/NextBusXMLFeed.pdf#page=7) |
| [List Vehicle Locations](actions/list-vehicle-locations.md) | `GET /publicXMLFeed` | [docs](https://retro.umoiq.com/xmlFeedDocs/NextBusXMLFeed.pdf#page=20) |
