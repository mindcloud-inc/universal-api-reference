# <img src="https://images.mindcloud.co/apps/icons/bureau-of-labor-statistics-logo_1777495674198.png" alt="Bureau of Labor Statistics logo" width="28" height="28"> Bureau of Labor Statistics: Universal API

Access public U.S. Bureau of Labor Statistics time-series data, popular series, and survey metadata through the BLS Public Data API.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/bureauOfLaborStatistics/latest
- **Actions:** 6
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.bls.gov/
- **Vendor API docs:** https://www.bls.gov/developers/home.htm

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Latest Series Data](actions/get-latest-series-data.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/bureauOfLaborStatistics/latest/actions/get-latest-series-data?connectionId=$CONNECTION_ID&seriesId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (6)

### Bls Latest Series Data

| Action | Method | Description |
| --- | --- | --- |
| [Get Latest Series Data](actions/get-latest-series-data.md) | GET | Retrieves the latest data point for a Bureau of Labor Statistics series. |

### Bls Popular Series

| Action | Method | Description |
| --- | --- | --- |
| [List Popular Series](actions/list-popular-series.md) | GET | Retrieves popular Bureau of Labor Statistics series IDs. |

### Bls Series Data

| Action | Method | Description |
| --- | --- | --- |
| [Get Single Series Data](actions/get-single-series-data.md) | GET | Retrieves recent data for one Bureau of Labor Statistics series. |

### Bls Series Data Query

| Action | Method | Description |
| --- | --- | --- |
| [Query Series Data](actions/query-series-data.md) | GET | Finds Bureau of Labor Statistics data for one or more series. |

### Bls Survey

| Action | Method | Description |
| --- | --- | --- |
| [Get Survey](actions/get-survey.md) | GET | Retrieves metadata for a Bureau of Labor Statistics survey. |

### Bls Surveys

| Action | Method | Description |
| --- | --- | --- |
| [List Surveys](actions/list-surveys.md) | GET | Retrieves metadata for all Bureau of Labor Statistics surveys. |

