# <img src="https://images.mindcloud.co/apps/icons/u-sgsearthquake-hazards_1777928009678.png" alt="USGS Earthquake Hazards logo" width="28" height="28"> USGS Earthquake Hazards: Universal API

Search earthquake events, feeds, catalogs, and region data

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/uSGSEarthquakeHazards/latest
- **Category:** Business Intelligence / Data Extraction
- **Actions:** 24
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://earthquake.usgs.gov/earthquakes/
- **Vendor API docs:** https://earthquake.usgs.gov/fdsnws/event/1/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Search Earthquakes](actions/search-earthquakes.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/uSGSEarthquakeHazards/latest/actions/search-earthquakes?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (24)

### Earthquake Catalog

| Action | Method | Description |
| --- | --- | --- |
| [List Earthquake Catalogs](actions/list-earthquake-catalogs.md) | GET | Retrieves available earthquake catalogs from USGS Earthquake Hazards. |

### Earthquake Contributor

| Action | Method | Description |
| --- | --- | --- |
| [List Earthquake Contributors](actions/list-earthquake-contributors.md) | GET | Retrieves available earthquake contributors from USGS Earthquake Hazards. |

### Earthquake Event

| Action | Method | Description |
| --- | --- | --- |
| [Get All Earthquakes Past Day](actions/get-all-earthquakes-past-day.md) | GET | Retrieves all earthquakes from the past day. |
| [Get All Earthquakes Past Hour](actions/get-all-earthquakes-past-hour.md) | GET | Retrieves all earthquakes from the past hour. |
| [Get All Earthquakes Past Month](actions/get-all-earthquakes-past-month.md) | GET | Retrieves all earthquakes from the past 30 days. |
| [Get All Earthquakes Past Week](actions/get-all-earthquakes-past-week.md) | GET | Retrieves all earthquakes from the past week. |
| [Get Earthquake By Event ID](actions/get-earthquake-by-event-id.md) | GET | Finds an earthquake in USGS Earthquake Hazards by event ID. |
| [Get M1.0+ Earthquakes Past Day](actions/get-m10-earthquakes-past-day.md) | GET | Retrieves M1.0+ earthquakes from the past day. |
| [Get M1.0+ Earthquakes Past Hour](actions/get-m10-earthquakes-past-hour.md) | GET | Retrieves M1.0+ earthquakes from the past hour. |
| [Get M2.5+ Earthquakes Past Day](actions/get-m25-earthquakes-past-day.md) | GET | Retrieves M2.5+ earthquakes from the past day. |
| [Get M2.5+ Earthquakes Past Hour](actions/get-m25-earthquakes-past-hour.md) | GET | Retrieves M2.5+ earthquakes from the past hour. |
| [Get M2.5+ Earthquakes Past Week](actions/get-m25-earthquakes-past-week.md) | GET | Retrieves M2.5+ earthquakes from the past week. |
| [Get M4.5+ Earthquakes Past Day](actions/get-m45-earthquakes-past-day.md) | GET | Retrieves M4.5+ earthquakes from the past day. |
| [Get M4.5+ Earthquakes Past Hour](actions/get-m45-earthquakes-past-hour.md) | GET | Retrieves M4.5+ earthquakes from the past hour. |
| [Get M4.5+ Earthquakes Past Week](actions/get-m45-earthquakes-past-week.md) | GET | Retrieves M4.5+ earthquakes from the past week. |
| [Get Significant Earthquakes Past Day](actions/get-significant-earthquakes-past-day.md) | GET | Retrieves significant earthquakes from the past day. |
| [Get Significant Earthquakes Past Hour](actions/get-significant-earthquakes-past-hour.md) | GET | Retrieves significant earthquakes from the past hour. |
| [Get Significant Earthquakes Past Month](actions/get-significant-earthquakes-past-month.md) | GET | Retrieves significant earthquakes from the past 30 days. |
| [Get Significant Earthquakes Past Week](actions/get-significant-earthquakes-past-week.md) | GET | Retrieves significant earthquakes from the past week. |
| [Search Earthquakes](actions/search-earthquakes.md) | GET | Finds earthquakes in USGS Earthquake Hazards by search parameters. |

### Earthquake Event Count

| Action | Method | Description |
| --- | --- | --- |
| [Count Earthquakes](actions/count-earthquakes.md) | GET | Counts earthquakes matching a USGS Earthquake Hazards query. |

### Earthquake Region

| Action | Method | Description |
| --- | --- | --- |
| [Get Regions For Coordinates](actions/get-regions-for-coordinates.md) | GET | Retrieves regions for latitude and longitude coordinates. |

### Event Api Parameters

| Action | Method | Description |
| --- | --- | --- |
| [Get Event API Parameters](actions/get-event-api-parameters.md) | GET | Retrieves event API parameters from USGS Earthquake Hazards. |

### Event Service Version

| Action | Method | Description |
| --- | --- | --- |
| [Get Event Service Version](actions/get-event-service-version.md) | GET | Retrieves the event service version from USGS Earthquake Hazards. |

