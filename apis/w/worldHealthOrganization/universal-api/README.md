# <img src="https://images.mindcloud.co/apps/icons/world-health-organization_1776364321591.png" alt="World Health Organization logo" width="28" height="28"> World Health Organization: Universal API

Access World Health Organization Global Health Observatory data through WHO's public OData API, including indicators, dimensions, dimension values, regions, countries, and indicator observations.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/worldHealthOrganization/latest
- **Category:** Business Intelligence / Analytics & BI
- **Actions:** 16
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.who.int/
- **Vendor API docs:** https://www.who.int/data/gho/info/gho-odata-api

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Dimension](actions/get-dimension.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/worldHealthOrganization/latest/actions/get-dimension?connectionId=$CONNECTION_ID&dimensionCode=REGION" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (16)

### Age Group Dimension Value

| Action | Method | Description |
| --- | --- | --- |
| [List Age Groups](actions/list-age-groups.md) | GET | Retrieves age groups from the World Health Organization. |

### Country

| Action | Method | Description |
| --- | --- | --- |
| [List Countries](actions/list-countries.md) | GET | Retrieves countries from the World Health Organization. |

### Dimension

| Action | Method | Description |
| --- | --- | --- |
| [Get Dimension](actions/get-dimension.md) | GET | Retrieves a dimension from the World Health Organization. |
| [List Dimensions](actions/list-dimensions.md) | GET | Retrieves dimensions from the World Health Organization. |

### Dimension Value

| Action | Method | Description |
| --- | --- | --- |
| [List Dimension Values](actions/list-dimension-values.md) | GET | Retrieves values for a dimension from the World Health Organization. |

### Income Group Dimension Value

| Action | Method | Description |
| --- | --- | --- |
| [List Income Groups](actions/list-income-groups.md) | GET | Retrieves income groups from the World Health Organization. |

### Indicator

| Action | Method | Description |
| --- | --- | --- |
| [Get Indicator](actions/get-indicator.md) | GET | Retrieves an indicator from the World Health Organization. |
| [List Indicators](actions/list-indicators.md) | GET | Retrieves indicators from the World Health Organization. |

### Indicator Dimension

| Action | Method | Description |
| --- | --- | --- |
| [List Indicator Dimensions](actions/list-indicator-dimensions.md) | GET | Retrieves indicator dimensions from the World Health Organization. |

### Indicator Observation

| Action | Method | Description |
| --- | --- | --- |
| [List Indicator Data](actions/list-indicator-data.md) | GET | Retrieves data for an indicator from the World Health Organization. |

### Odata Entity Set

| Action | Method | Description |
| --- | --- | --- |
| [List OData Entity Sets](actions/list-odata-entity-sets.md) | GET | Retrieves OData entity sets from the World Health Organization. |

### Publish State

| Action | Method | Description |
| --- | --- | --- |
| [List Publish States](actions/list-publish-states.md) | GET | Retrieves publish states from the World Health Organization. |

### Region Country

| Action | Method | Description |
| --- | --- | --- |
| [List Region Countries](actions/list-region-countries.md) | GET | Retrieves region-country mappings from the World Health Organization. |

### Sex Dimension Value

| Action | Method | Description |
| --- | --- | --- |
| [List Sex Values](actions/list-sex-values.md) | GET | Retrieves sex values from the World Health Organization. |

### Who Region

| Action | Method | Description |
| --- | --- | --- |
| [List WHO Regions](actions/list-who-regions.md) | GET | Retrieves WHO regions from the World Health Organization. |

### Year Dimension Value

| Action | Method | Description |
| --- | --- | --- |
| [List Year Values](actions/list-year-values.md) | GET | Retrieves year values from the World Health Organization. |

