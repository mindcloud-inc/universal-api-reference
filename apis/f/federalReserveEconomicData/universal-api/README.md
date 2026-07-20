# <img src="https://images.mindcloud.co/apps/icons/federal-reserve-economic-data_1777478716020.png" alt="Federal Reserve Economic Data logo" width="28" height="28"> Federal Reserve Economic Data: Universal API

FRED is the Federal Reserve Bank of St. Louis API for querying Federal Reserve Economic Data and ALFRED economic time series over HTTPS in XML or JSON.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/federalReserveEconomicData/latest
- **Category:** Business Intelligence / Analytics & BI
- **Actions:** 20
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://fred.stlouisfed.org
- **Vendor API docs:** https://fred.stlouisfed.org/docs/api/fred/overview.html

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Sources](actions/list-sources.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/federalReserveEconomicData/latest/actions/list-sources?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (20)

### Category

| Action | Method | Description |
| --- | --- | --- |
| [Get Category](actions/get-category.md) | GET | Retrieves a category from Federal Reserve Economic Data. |
| [List Category Children](actions/list-category-children.md) | GET | Retrieves child categories from Federal Reserve Economic Data. |
| [List Related Categories](actions/list-related-categories.md) | GET | Retrieves related categories from Federal Reserve Economic Data. |
| [List Series Categories](actions/list-series-categories.md) | GET | Retrieves categories for a series from Federal Reserve Economic Data. |

### Observation

| Action | Method | Description |
| --- | --- | --- |
| [List Series Observations](actions/list-series-observations.md) | GET | Retrieves series observations from Federal Reserve Economic Data. |

### Release

| Action | Method | Description |
| --- | --- | --- |
| [Get Release](actions/get-release.md) | GET | Retrieves a release from Federal Reserve Economic Data. |
| [Get Series Release](actions/get-series-release.md) | GET | Retrieves the release for a series from Federal Reserve Economic Data. |
| [List Releases](actions/list-releases.md) | GET | Retrieves releases from Federal Reserve Economic Data. |
| [List Source Releases](actions/list-source-releases.md) | GET | Retrieves releases for a source from Federal Reserve Economic Data. |

### Release Date

| Action | Method | Description |
| --- | --- | --- |
| [List Release Dates](actions/list-release-dates.md) | GET | Retrieves release dates from Federal Reserve Economic Data. |
| [List Release Dates For Release](actions/list-release-dates-for-release.md) | GET | Retrieves release dates for a release from Federal Reserve Economic Data. |

### Series

| Action | Method | Description |
| --- | --- | --- |
| [Get Series](actions/get-series.md) | GET | Retrieves a series from Federal Reserve Economic Data. |
| [List Category Series](actions/list-category-series.md) | GET | Retrieves series for a category from Federal Reserve Economic Data. |
| [List Release Series](actions/list-release-series.md) | GET | Retrieves series for a release from Federal Reserve Economic Data. |
| [List Series Updates](actions/list-series-updates.md) | GET | Retrieves series updates from Federal Reserve Economic Data. |
| [Search Series](actions/search-series.md) | GET | Finds series in Federal Reserve Economic Data by search text. |

### Source

| Action | Method | Description |
| --- | --- | --- |
| [Get Source](actions/get-source.md) | GET | Retrieves a source from Federal Reserve Economic Data. |
| [List Release Sources](actions/list-release-sources.md) | GET | Retrieves sources for a release from Federal Reserve Economic Data. |
| [List Sources](actions/list-sources.md) | GET | Retrieves sources from Federal Reserve Economic Data. |

### Tag

| Action | Method | Description |
| --- | --- | --- |
| [List Category Tags](actions/list-category-tags.md) | GET | Retrieves category tags from Federal Reserve Economic Data. |

