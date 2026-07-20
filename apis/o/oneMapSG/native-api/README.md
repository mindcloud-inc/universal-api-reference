# OneMap SG: Native API Reference

A consolidated summary of OneMap SG's API configuration and 24 documented operations, with links to official documentation.

- **Official docs:** https://www.onemap.gov.sg/apidocs/
- **API base URL:** `https://www.onemap.gov.sg`

## Authentication

### OneMap Account

Authenticate with your OneMap account email and password to obtain the access token required for most OneMap API requests.

### Credentials

- **Email Address:** `email` · required · The email address for your OneMap account.
- **Password:** `password` · required · The password for your OneMap account.

Send these headers with each API request:

```http
Authorization: Bearer <custom.accessToken>
```

[Official authentication documentation](https://www.onemap.gov.sg/apidocs/authentication)

## Endpoints (24 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Check Theme Status](actions/check-theme-status.md) | `GET /api/public/themesvc/checkThemeStatus` | [docs](https://www.onemap.gov.sg/apidocs/themes) |
| [Convert SVY21 to EPSG:3857](actions/convert3414-to3857.md) | `GET /api/common/convert/3414to3857` | [docs](https://www.onemap.gov.sg/apidocs/coordinate) |
| [Convert SVY21 to WGS84](actions/convert3414-to4326.md) | `GET /api/common/convert/3414to4326` | [docs](https://www.onemap.gov.sg/apidocs/coordinate) |
| [Convert EPSG:3857 to SVY21](actions/convert3857-to3414.md) | `GET /api/common/convert/3857to3414` | [docs](https://www.onemap.gov.sg/apidocs/coordinate) |
| [Convert EPSG:3857 to WGS84](actions/convert3857-to4326.md) | `GET /api/common/convert/3857to4326` | [docs](https://www.onemap.gov.sg/apidocs/coordinate) |
| [Convert WGS84 to SVY21](actions/convert4326-to3414.md) | `GET /api/common/convert/4326to3414` | [docs](https://www.onemap.gov.sg/apidocs/coordinate) |
| [Convert WGS84 to EPSG:3857](actions/convert4326-to3857.md) | `GET /api/common/convert/4326to3857` | [docs](https://www.onemap.gov.sg/apidocs/coordinate) |
| [Get All Planning Areas](actions/get-all-planning-areas.md) | `GET /api/public/popapi/getAllPlanningarea` | [docs](https://www.onemap.gov.sg/apidocs/planningarea) |
| [Get All Themes Info](actions/get-all-themes-info.md) | `GET /api/public/themesvc/getAllThemesInfo` | [docs](https://www.onemap.gov.sg/apidocs/themes) |
| [Get Auth Token](actions/get-auth-token.md) | `POST /api/auth/post/getToken` | [docs](https://www.onemap.gov.sg/apidocs/authentication) |
| [Get Nearest Bus Stops](actions/get-nearest-bus-stops.md) | `GET /api/public/nearbysvc/getNearestBusStops` | [docs](https://www.onemap.gov.sg/apidocs/nearbytransport) |
| [Get Nearest MRT Stops](actions/get-nearest-mrt-stops.md) | `GET /api/public/nearbysvc/getNearestMrtStops` | [docs](https://www.onemap.gov.sg/apidocs/nearbytransport) |
| [Get Planning Area by Coordinates](actions/get-planning-area-by-coordinates.md) | `GET /api/public/popapi/getPlanningarea` | [docs](https://www.onemap.gov.sg/apidocs/planningarea) |
| [Get Planning Area Names](actions/get-planning-area-names.md) | `GET /api/public/popapi/getPlanningareaNames` | [docs](https://www.onemap.gov.sg/apidocs/planningarea) |
| [Get Static Map](actions/get-static-map.md) | `GET /api/staticmap/getStaticImage` | [docs](https://www.onemap.gov.sg/apidocs/staticmap) |
| [Get Theme Info](actions/get-theme-info.md) | `GET /api/public/themesvc/getThemeInfo` | [docs](https://www.onemap.gov.sg/apidocs/themes) |
| [Retrieve Theme](actions/retrieve-theme.md) | `GET /api/public/themesvc/retrieveTheme` | [docs](https://www.onemap.gov.sg/apidocs/themes) |
| [Retrieve Theme Within Extents](actions/retrieve-theme-within-extents.md) | `GET /api/public/themesvc/retrieveTheme` | [docs](https://www.onemap.gov.sg/apidocs/themes) |
| [Reverse Geocode (Latitude and Longitude)](actions/reverse-geocode-lat-lng.md) | `GET /api/public/revgeocode` | [docs](https://www.onemap.gov.sg/apidocs/reversegeocode) |
| [Reverse Geocode (SVY21 Coordinates)](actions/reverse-geocode-svy21.md) | `GET /api/public/revgeocodexy` | [docs](https://www.onemap.gov.sg/apidocs/reversegeocode) |
| [Route (Barrier-Free)](actions/route-barrier-free.md) | `GET /api/bfa/routingsvc/route` | [docs](https://www.onemap.gov.sg/apidocs/bfa) |
| [Route (Public Transport)](actions/route-public-transport.md) | `GET /api/public/routingsvc/route` | [docs](https://www.onemap.gov.sg/apidocs/routing) |
| [Route (Walk, Drive, or Cycle)](actions/route-walk-drive-cycle.md) | `GET /api/public/routingsvc/route` | [docs](https://www.onemap.gov.sg/apidocs/routing) |
| [Search Locations](actions/search-locations.md) | `GET /api/common/elastic/search` | [docs](https://www.onemap.gov.sg/apidocs/search) |
