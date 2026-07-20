# <img src="https://images.mindcloud.co/apps/icons/climatiq-icon_1777493014949.jpeg" alt="Climatiq logo" width="28" height="28"> Climatiq: Universal API

Climatiq calculates carbon emissions and CO2e estimates from activity data, energy use, freight, procurement spend, industry classifications, and emission-factor reference data.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/climatiq/latest
- **Category:** Support / Field Service
- **Actions:** 4
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.climatiq.io
- **Vendor API docs:** https://www.climatiq.io/docs

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Data Versions](actions/get-data-versions.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/climatiq/latest/actions/get-data-versions?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (4)

### Data Version

| Action | Method | Description |
| --- | --- | --- |
| [Get Data Versions](actions/get-data-versions.md) | GET | Retrieves available data versions from Climatiq. |

### Emission Estimate

| Action | Method | Description |
| --- | --- | --- |
| [Estimate Emissions](actions/estimate-emissions.md) | POST | Estimates emissions in Climatiq from activity data. |

### Emission Factor

| Action | Method | Description |
| --- | --- | --- |
| [Search Emission Factors](actions/search-emission-factors.md) | GET | Finds emission factors in Climatiq by search criteria. |

### Unit Type

| Action | Method | Description |
| --- | --- | --- |
| [Get Unit Types](actions/get-unit-types.md) | GET | Retrieves available unit types from Climatiq. |

