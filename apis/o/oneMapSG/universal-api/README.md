# <img src="https://images.mindcloud.co/apps/icons/one-map-sg_1776966513724.png" alt="OneMap SG logo" width="28" height="28"> OneMap SG: Universal API

Search Singapore addresses, routes, planning areas, transport stops, themes, and static maps with the official OneMap API.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/oneMapSG/latest
- **Category:** Support / Field Service
- **Actions:** 24
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.onemap.gov.sg/
- **Vendor API docs:** https://www.onemap.gov.sg/apidocs/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Check Theme Status](actions/check-theme-status.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/oneMapSG/latest/actions/check-theme-status?connectionId=$CONNECTION_ID&queryName=kindergartens&dateTime=2023-06-15T16%3A00%3A00.000Z" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (24)

### Access Token

| Action | Method | Description |
| --- | --- | --- |
| [Get Auth Token](actions/get-auth-token.md) | POST | Creates an authentication token in OneMap SG. |

### Address

| Action | Method | Description |
| --- | --- | --- |
| [Reverse Geocode (Latitude and Longitude)](actions/reverse-geocode-lat-lng.md) | GET | Retrieves an address from OneMap SG by latitude and longitude. |
| [Reverse Geocode (SVY21 Coordinates)](actions/reverse-geocode-svy21.md) | GET | Retrieves an address from OneMap SG by SVY21 coordinates. |

### Bus Stop

| Action | Method | Description |
| --- | --- | --- |
| [Get Nearest Bus Stops](actions/get-nearest-bus-stops.md) | GET | Retrieves nearest bus stops from OneMap SG. |

### Coordinate

| Action | Method | Description |
| --- | --- | --- |
| [Convert SVY21 to EPSG:3857](actions/convert3414-to3857.md) | GET | Converts SVY21 coordinates to EPSG:3857 in OneMap SG. |
| [Convert SVY21 to WGS84](actions/convert3414-to4326.md) | GET | Converts SVY21 coordinates to WGS84 in OneMap SG. |
| [Convert EPSG:3857 to SVY21](actions/convert3857-to3414.md) | GET | Converts EPSG:3857 coordinates to SVY21 in OneMap SG. |
| [Convert EPSG:3857 to WGS84](actions/convert3857-to4326.md) | GET | Converts EPSG:3857 coordinates to WGS84 in OneMap SG. |
| [Convert WGS84 to SVY21](actions/convert4326-to3414.md) | GET | Converts WGS84 coordinates to SVY21 in OneMap SG. |
| [Convert WGS84 to EPSG:3857](actions/convert4326-to3857.md) | GET | Converts WGS84 coordinates to EPSG:3857 in OneMap SG. |

### Location

| Action | Method | Description |
| --- | --- | --- |
| [Search Locations](actions/search-locations.md) | GET | Finds locations in OneMap SG by search value. |

### Mrt Stop

| Action | Method | Description |
| --- | --- | --- |
| [Get Nearest MRT Stops](actions/get-nearest-mrt-stops.md) | GET | Retrieves nearest MRT stops from OneMap SG. |

### Planning Area

| Action | Method | Description |
| --- | --- | --- |
| [Get All Planning Areas](actions/get-all-planning-areas.md) | GET | Retrieves all planning areas from OneMap SG. |
| [Get Planning Area by Coordinates](actions/get-planning-area-by-coordinates.md) | GET | Retrieves a planning area from OneMap SG by coordinates. |
| [Get Planning Area Names](actions/get-planning-area-names.md) | GET | Retrieves planning area names from OneMap SG. |

### Route

| Action | Method | Description |
| --- | --- | --- |
| [Route (Barrier-Free)](actions/route-barrier-free.md) | GET | Retrieves a barrier-free route from OneMap SG. |
| [Route (Public Transport)](actions/route-public-transport.md) | GET | Retrieves a public transport route from OneMap SG. |
| [Route (Walk, Drive, or Cycle)](actions/route-walk-drive-cycle.md) | GET | Retrieves a walking, driving, or cycling route from OneMap SG. |

### Static Map

| Action | Method | Description |
| --- | --- | --- |
| [Get Static Map](actions/get-static-map.md) | GET | Retrieves a static map image from OneMap SG. |

### Theme

| Action | Method | Description |
| --- | --- | --- |
| [Get All Themes Info](actions/get-all-themes-info.md) | GET | Retrieves information about all OneMap SG themes. |
| [Get Theme Info](actions/get-theme-info.md) | GET | Retrieves information about a OneMap SG theme. |
| [Retrieve Theme](actions/retrieve-theme.md) | GET | Retrieves theme data from OneMap SG. |
| [Retrieve Theme Within Extents](actions/retrieve-theme-within-extents.md) | GET | Retrieves OneMap SG theme data within map extents. |

### Theme Status

| Action | Method | Description |
| --- | --- | --- |
| [Check Theme Status](actions/check-theme-status.md) | GET | Retrieves the status of a OneMap SG theme. |

