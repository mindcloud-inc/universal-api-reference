# <img src="https://images.mindcloud.co/apps/icons/clinical-trialsgov_1776366299122.png" alt="ClinicalTrials.gov logo" width="28" height="28"> ClinicalTrials.gov: Universal API

ClinicalTrials.gov is the U.S. National Library of Medicine's public registry and results database for clinical studies. This app wraps the modernized ClinicalTrials.gov REST API v2 for study search, record retrieval, metadata, search areas, enums, and statistics.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/clinicalTrialsgov/latest
- **Category:** Productivity / Knowledge Management
- **Actions:** 14
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://clinicaltrials.gov/
- **Vendor API docs:** https://clinicaltrials.gov/data-api/api

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get API Version](actions/get-api-version.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/clinicalTrialsgov/latest/actions/get-api-version?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (14)

### Database Statistic

| Action | Method | Description |
| --- | --- | --- |
| [Get Database Size Statistics](actions/get-database-size-statistics.md) | GET |  |

### Enum

| Action | Method | Description |
| --- | --- | --- |
| [Get Enums](actions/get-enums.md) | GET |  |

### Field Size Statistic

| Action | Method | Description |
| --- | --- | --- |
| [Get Field Size Statistics](actions/get-field-size-statistics.md) | GET |  |

### Field Value Statistic

| Action | Method | Description |
| --- | --- | --- |
| [Get Field Value Statistics](actions/get-field-value-statistics.md) | GET |  |

### Metadata Field

| Action | Method | Description |
| --- | --- | --- |
| [Get Studies Metadata](actions/get-studies-metadata.md) | GET |  |

### Search Area

| Action | Method | Description |
| --- | --- | --- |
| [Get Search Areas](actions/get-search-areas.md) | GET |  |

### Study

| Action | Method | Description |
| --- | --- | --- |
| [Get Study](actions/get-study.md) | GET |  |
| [Search Studies](actions/search-studies.md) | GET |  |

### Unknown Objects

| Action | Method | Description |
| --- | --- | --- |
| [Get Study CSV](actions/get-study-csv.md) | GET |  |
| [Get Study FHIR JSON](actions/get-study-fhir-json.md) | GET |  |
| [Get Study JSON ZIP](actions/get-study-json-zip.md) | GET |  |
| [Get Study RIS](actions/get-study-ris.md) | GET |  |
| [Search Studies CSV](actions/search-studies-csv.md) | GET |  |

### Version

| Action | Method | Description |
| --- | --- | --- |
| [Get API Version](actions/get-api-version.md) | GET |  |

