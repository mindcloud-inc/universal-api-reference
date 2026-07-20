# <img src="https://images.mindcloud.co/apps/icons/n-ceiclimate-data_1777544962862.png" alt="NCEI Climate Data logo" width="28" height="28"> NCEI Climate Data: Universal API

Access NOAA NCEI Climate Data Online datasets, locations, stations, data types, and observed climate data through the CDO Web Services API v2.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/nCEIClimateData/latest
- **Actions:** 13
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.ncei.noaa.gov/cdo-web/
- **Vendor API docs:** https://www.ncei.noaa.gov/cdo-web/webservices/v2

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Datasets](actions/list-datasets.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/nCEIClimateData/latest/actions/list-datasets?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (13)

### Climate Data

| Action | Method | Description |
| --- | --- | --- |
| [List Climate Data](actions/list-climate-data.md) | GET | Finds climate data in NCEI Climate Data by dataset and date range. |

### Data Category

| Action | Method | Description |
| --- | --- | --- |
| [Get Data Category](actions/get-data-category.md) | GET | Retrieves data category details from NCEI Climate Data. |
| [List Data Categories](actions/list-data-categories.md) | GET | Finds data categories in NCEI Climate Data by filter criteria. |

### Data Type

| Action | Method | Description |
| --- | --- | --- |
| [Get Data Type](actions/get-data-type.md) | GET | Retrieves data type details from NCEI Climate Data. |
| [List Data Types](actions/list-data-types.md) | GET | Finds data types in NCEI Climate Data by filter criteria. |

### Dataset

| Action | Method | Description |
| --- | --- | --- |
| [Get Dataset](actions/get-dataset.md) | GET | Retrieves dataset details from NCEI Climate Data. |
| [List Datasets](actions/list-datasets.md) | GET | Finds climate datasets in NCEI Climate Data by filter criteria. |

### Location

| Action | Method | Description |
| --- | --- | --- |
| [Get Location](actions/get-location.md) | GET | Retrieves location details from NCEI Climate Data. |
| [List Locations](actions/list-locations.md) | GET | Finds locations in NCEI Climate Data by filter criteria. |

### Location Category

| Action | Method | Description |
| --- | --- | --- |
| [Get Location Category](actions/get-location-category.md) | GET | Retrieves location category details from NCEI Climate Data. |
| [List Location Categories](actions/list-location-categories.md) | GET | Finds location categories in NCEI Climate Data by filter criteria. |

### Station

| Action | Method | Description |
| --- | --- | --- |
| [Get Station](actions/get-station.md) | GET | Retrieves station details from NCEI Climate Data. |
| [List Stations](actions/list-stations.md) | GET | Finds weather stations in NCEI Climate Data by filter criteria. |

