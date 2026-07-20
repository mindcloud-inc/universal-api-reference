# <img src="https://images.mindcloud.co/apps/icons/international-monetary-fund_1776697000399.png" alt="International Monetary Fund logo" width="28" height="28"> International Monetary Fund: Universal API

Public IMF DataMapper API for indicators, countries, regions, analytical groups, and time-series macroeconomic data published by the International Monetary Fund.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/internationalMonetaryFund/latest
- **Category:** Business Intelligence / Analytics & BI
- **Actions:** 6
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.imf.org/en/Data
- **Vendor API docs:** https://www.imf.org/external/datamapper/api/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Indicators](actions/list-indicators.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/internationalMonetaryFund/latest/actions/list-indicators?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (6)

### Analytical Group

| Action | Method | Description |
| --- | --- | --- |
| [List Analytical Groups](actions/list-analytical-groups.md) | GET | Retrieves defined analytical groups from the IMF DataMapper API. |

### Country

| Action | Method | Description |
| --- | --- | --- |
| [List Countries](actions/list-countries.md) | GET | Retrieves available countries from the IMF DataMapper API. |

### Indicator

| Action | Method | Description |
| --- | --- | --- |
| [List Indicators](actions/list-indicators.md) | GET | Retrieves available indicators from the IMF DataMapper API. |

### Indicator Time Series

| Action | Method | Description |
| --- | --- | --- |
| [Get Indicator Time Series](actions/get-indicator-time-series.md) | GET | Retrieves IMF time series for a single indicator. |

### Region

| Action | Method | Description |
| --- | --- | --- |
| [List Regions](actions/list-regions.md) | GET | Retrieves defined regions from the IMF DataMapper API. |

### Scoped Indicator Time Series

| Action | Method | Description |
| --- | --- | --- |
| [Get Scoped Time Series](actions/get-scoped-time-series.md) | GET | Retrieves IMF time series by country, region, or group. |

