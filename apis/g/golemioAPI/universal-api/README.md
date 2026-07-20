# <img src="https://images.mindcloud.co/apps/icons/golemio_1777325262312.png" alt="Golemio API logo" width="28" height="28"> Golemio API: Universal API

Access real-time and open data from the Golemio Prague Data Platform, including city infrastructure, mobility, parking, waste, environmental, and public-service datasets.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/golemioAPI/latest
- **Actions:** 15
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.golemio.cz/
- **Vendor API docs:** https://operator-ict.gitlab.io/golemio/documentation/en/open-data-api/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Parking Sources](actions/list-parking-sources.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/golemioAPI/latest/actions/list-parking-sources?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (15)

### Air Quality Station

| Action | Method | Description |
| --- | --- | --- |
| [List Air Quality Stations](actions/list-air-quality-stations.md) | GET | Finds air quality stations in the Golemio API. |

### Air Quality Station History

| Action | Method | Description |
| --- | --- | --- |
| [List Air Quality Station History](actions/list-air-quality-station-history.md) | GET | Finds air quality station history in the Golemio API. |

### Bicycle Counter

| Action | Method | Description |
| --- | --- | --- |
| [List Bicycle Counters](actions/list-bicycle-counters.md) | GET | Finds bicycle counters in the Golemio API. |

### City District

| Action | Method | Description |
| --- | --- | --- |
| [List City Districts](actions/list-city-districts.md) | GET | Finds city districts in the Golemio API. |

### Garden

| Action | Method | Description |
| --- | --- | --- |
| [List Gardens](actions/list-gardens.md) | GET | Finds gardens in the Golemio API. |

### Medical Institution

| Action | Method | Description |
| --- | --- | --- |
| [List Medical Institutions](actions/list-medical-institutions.md) | GET | Finds medical institutions in the Golemio API. |

### Municipal Authority

| Action | Method | Description |
| --- | --- | --- |
| [List Municipal Authorities](actions/list-municipal-authorities.md) | GET | Finds municipal authorities in the Golemio API. |

### Municipal Library

| Action | Method | Description |
| --- | --- | --- |
| [List Municipal Libraries](actions/list-municipal-libraries.md) | GET | Finds municipal libraries in the Golemio API. |

### Municipal Police Station

| Action | Method | Description |
| --- | --- | --- |
| [List Municipal Police Stations](actions/list-municipal-police-stations.md) | GET | Finds municipal police stations in the Golemio API. |

### Parking Location

| Action | Method | Description |
| --- | --- | --- |
| [List Parking Locations](actions/list-parking-locations.md) | GET | Finds parking locations in the Golemio API. |

### Parking Machine

| Action | Method | Description |
| --- | --- | --- |
| [List Parking Machines](actions/list-parking-machines.md) | GET | Finds parking machines in the Golemio API. |

### Parking Measurement

| Action | Method | Description |
| --- | --- | --- |
| [List Parking Measurements](actions/list-parking-measurements.md) | GET | Finds parking measurements in the Golemio API. |

### Parking Source

| Action | Method | Description |
| --- | --- | --- |
| [List Parking Sources](actions/list-parking-sources.md) | GET | Finds parking sources in the Golemio API. |

### Parking Tariff

| Action | Method | Description |
| --- | --- | --- |
| [List Parking Tariffs](actions/list-parking-tariffs.md) | GET | Finds parking tariffs in the Golemio API. |

### Waste Collection Station

| Action | Method | Description |
| --- | --- | --- |
| [List Waste Collection Stations](actions/list-waste-collection-stations.md) | GET | Finds waste collection stations in the Golemio API. |

