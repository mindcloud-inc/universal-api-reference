# <img src="https://images.mindcloud.co/apps/icons/daily-med-logo_1777482396223.png" alt="DailyMed logo" width="28" height="28"> DailyMed: Universal API

Access current DailyMed Structured Product Labeling (SPL) information, including drug labels, NDCs, RxCUIs, drug classes, application numbers, media links, packaging, and ingredient identifiers from the National Library of Medicine.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/dailyMed/latest
- **Category:** Business Intelligence / Data Extraction
- **Actions:** 12
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://dailymed.nlm.nih.gov/dailymed/
- **Vendor API docs:** https://dailymed.nlm.nih.gov/dailymed/app-support-web-services.cfm

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List SPLs](actions/list-spls.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/dailyMed/latest/actions/list-spls?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (12)

### Application Number

| Action | Method | Description |
| --- | --- | --- |
| [List Application Numbers](actions/list-application-numbers.md) | GET | Retrieves application numbers from DailyMed. |

### Drug Class

| Action | Method | Description |
| --- | --- | --- |
| [List Drug Classes](actions/list-drug-classes.md) | GET | Retrieves drug classes from DailyMed. |

### Drug Name

| Action | Method | Description |
| --- | --- | --- |
| [List Drug Names](actions/list-drug-names.md) | GET | Retrieves drug names from DailyMed. |

### Ndc

| Action | Method | Description |
| --- | --- | --- |
| [List NDCs](actions/list-ndcs.md) | GET | Retrieves NDCs from DailyMed. |

### Rxcui

| Action | Method | Description |
| --- | --- | --- |
| [List RxCUIs](actions/list-rxcuis.md) | GET | Retrieves RxCUIs from DailyMed. |

### Spl

| Action | Method | Description |
| --- | --- | --- |
| [List SPLs](actions/list-spls.md) | GET | Retrieves SPLs from DailyMed. |

### Spl History

| Action | Method | Description |
| --- | --- | --- |
| [List SPL History](actions/list-spl-history.md) | GET | Retrieves SPL version history from DailyMed. |

### Spl Media

| Action | Method | Description |
| --- | --- | --- |
| [List SPL Media](actions/list-spl-media.md) | GET | Retrieves SPL media from DailyMed. |

### Spl Ndc

| Action | Method | Description |
| --- | --- | --- |
| [List SPL NDCs](actions/list-spl-ndcs.md) | GET | Retrieves NDCs for an SPL from DailyMed. |

### Spl Packaging

| Action | Method | Description |
| --- | --- | --- |
| [List SPL Packaging](actions/list-spl-packaging.md) | GET | Retrieves SPL packaging details from DailyMed. |

### Spl Xml Document

| Action | Method | Description |
| --- | --- | --- |
| [Get SPL XML Document](actions/get-spl-xml-document.md) | GET | Retrieves an SPL XML document from DailyMed. |

### Unii

| Action | Method | Description |
| --- | --- | --- |
| [List UNIIs](actions/list-uniis.md) | GET | Retrieves UNIIs from DailyMed. |

