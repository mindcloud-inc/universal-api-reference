# <img src="https://images.mindcloud.co/apps/icons/zillow-econ_1776963354872.png" alt="Zillow Econ logo" width="28" height="28"> Zillow Econ: Universal API

Bridge-hosted Zillow economic data access. Requires a Bridge account and approved Zillow Econ datasets.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/zillowEcon/latest
- **Category:** Business Intelligence / Data Extraction
- **Actions:** 3
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://bridgedataoutput.com/docs/explorer/zillow-group-econ-data
- **Vendor API docs:** https://bridgedataoutput.com/docs/platform

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get region metadata](actions/get-region-metadata.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/zillowEcon/latest/actions/get-region-metadata?connectionId=$CONNECTION_ID&stateCodeFIPS=48" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (3)

### Locations

| Action | Method | Description |
| --- | --- | --- |
| [Get region metadata](actions/get-region-metadata.md) | GET | Retrieves region metadata from Zillow Econ. |

### Metrics

| Action | Method | Description |
| --- | --- | --- |
| [Get market type metadata](actions/get-market-type-metadata.md) | GET | Retrieves market type metadata from Zillow Econ. |

### Reports

| Action | Method | Description |
| --- | --- | --- |
| [Get market report](actions/get-market-report.md) | GET | Retrieves market report data from Zillow Econ. |

