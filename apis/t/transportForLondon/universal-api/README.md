# <img src="https://images.mindcloud.co/apps/icons/tfl-icon_1777672087444.png" alt="Transport for London logo" width="28" height="28"> Transport for London: Universal API

Access Transport for London open data, including live line status, journey planning, stop points, arrivals, roads, bike points, places, occupancy, and search data from the TfL Unified API.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/transportForLondon/latest
- **Category:** Productivity / Scheduling
- **Actions:** 23
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://tfl.gov.uk
- **Vendor API docs:** https://api.tfl.gov.uk/swagger/ui/index.html

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Journey Modes](actions/journey-modes.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/transportForLondon/latest/actions/journey-modes?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (23)

### Arrival Prediction

| Action | Method | Description |
| --- | --- | --- |
| [Get Line Arrivals At Stop](actions/line-arrivals-at-stop.md) | GET | Retrieves line arrivals at a stop in Transport for London. |
| [Get Stop Arrivals](actions/stop-arrivals.md) | GET | Retrieves arrivals for a stop in Transport for London. |

### Bike Point

| Action | Method | Description |
| --- | --- | --- |
| [Get Bike Point](actions/bike-point.md) | GET | Retrieves a bike point from Transport for London. |
| [List Bike Points](actions/bike-points.md) | GET | Retrieves bike points from Transport for London. |

### Bike Point Search Result

| Action | Method | Description |
| --- | --- | --- |
| [Search Bike Points](actions/search-bike-points.md) | GET | Finds bike points in Transport for London by name. |

### Journey Mode

| Action | Method | Description |
| --- | --- | --- |
| [List Journey Modes](actions/journey-modes.md) | GET | Retrieves journey planner modes from Transport for London. |

### Journey Plan

| Action | Method | Description |
| --- | --- | --- |
| [Plan Journey](actions/plan-journey.md) | GET | Plans a journey between locations in Transport for London. |

### Line

| Action | Method | Description |
| --- | --- | --- |
| [Get Lines By Mode](actions/lines-by-mode.md) | GET | Retrieves lines for selected modes in Transport for London. |

### Line Disruption

| Action | Method | Description |
| --- | --- | --- |
| [Get Line Disruptions](actions/line-disruptions.md) | GET | Retrieves disruptions for selected lines in Transport for London. |

### Line Route

| Action | Method | Description |
| --- | --- | --- |
| [List Line Routes](actions/list-line-routes.md) | GET | Retrieves line routes from Transport for London. |

### Line Search Result

| Action | Method | Description |
| --- | --- | --- |
| [Search Lines](actions/search-lines.md) | GET | Finds lines or routes in Transport for London by query. |

### Line Status

| Action | Method | Description |
| --- | --- | --- |
| [Get Line Status By IDs](actions/line-status-by-ids.md) | GET | Retrieves line status for selected lines in Transport for London. |
| [Get Line Status By Mode](actions/line-status-by-mode.md) | GET | Retrieves line status for modes in Transport for London. |

### Nearby Stop Points

| Action | Method | Description |
| --- | --- | --- |
| [Find Nearby Stop Points](actions/nearby-stop-points.md) | GET | Finds nearby stop points in Transport for London. |

### Road

| Action | Method | Description |
| --- | --- | --- |
| [List Roads](actions/roads.md) | GET | Retrieves roads managed by Transport for London. |

### Road Disruption

| Action | Method | Description |
| --- | --- | --- |
| [Get Road Disruptions](actions/road-disruptions.md) | GET | Retrieves road disruptions for selected roads in Transport for London. |

### Road Status

| Action | Method | Description |
| --- | --- | --- |
| [Get Road Status](actions/road-status.md) | GET | Retrieves road status for selected roads in Transport for London. |

### Route Sequence

| Action | Method | Description |
| --- | --- | --- |
| [Get Line Route Sequence](actions/line-route-sequence.md) | GET | Retrieves a line route sequence from Transport for London. |

### Search Result

| Action | Method | Description |
| --- | --- | --- |
| [Search TfL](actions/search-tfl.md) | GET | Finds site results in Transport for London by query. |

### Stop Point

| Action | Method | Description |
| --- | --- | --- |
| [List Line Stop Points](actions/line-stop-points.md) | GET | Retrieves stop points served by a line in Transport for London. |
| [Get Stop Points By IDs](actions/stop-points-by-ids.md) | GET | Retrieves stop points by ID from Transport for London. |

### Stop Point Search Result

| Action | Method | Description |
| --- | --- | --- |
| [Search Stop Points](actions/search-stop-points.md) | GET | Finds stop points in Transport for London by name or code. |

### Stop Points Response

| Action | Method | Description |
| --- | --- | --- |
| [Get Stop Points By Mode](actions/stop-points-by-mode.md) | GET | Retrieves stop points for modes in Transport for London. |

