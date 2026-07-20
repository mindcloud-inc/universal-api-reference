# <img src="https://images.mindcloud.co/apps/icons/pappers_1774542319324.png" alt="Pappers logo" width="28" height="28"> Pappers: Universal API

Search companies, enrich records, and retrieve legal documents

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/pappers/latest
- **Category:** Business Intelligence / Data Extraction
- **Actions:** 16
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.pappers.fr
- **Vendor API docs:** https://www.pappers.fr/api/documentation

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get API Usage](actions/get-api-usage.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/pappers/latest/actions/get-api-usage?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (16)

### Api Usage

| Action | Method | Description |
| --- | --- | --- |
| [Get API Usage](actions/get-api-usage.md) | GET |  |

### Companies

| Action | Method | Description |
| --- | --- | --- |
| [Get Company](actions/get-company.md) | GET |  |
| [Get Company Accounts](actions/get-company-accounts.md) | GET |  |
| [Get Company Map](actions/get-company-map.md) | GET |  |
| [Get Company Suggestions](actions/get-company-suggestions.md) | GET |  |

### Company

| Action | Method | Description |
| --- | --- | --- |
| [Search Companies](actions/search-companies.md) | GET |  |

### Director

| Action | Method | Description |
| --- | --- | --- |
| [Search Directors](actions/search-directors.md) | GET |  |

### Document

| Action | Method | Description |
| --- | --- | --- |
| [Get INPI Extract](actions/get-inpi-extract.md) | GET |  |
| [Get INSEE Status Document](actions/get-insee-status-document.md) | GET |  |
| [Get Latest Statutes](actions/get-latest-statutes.md) | GET |  |
| [Get Pappers Extract](actions/get-pappers-extract.md) | GET |  |

### Documents

| Action | Method | Description |
| --- | --- | --- |
| [Get Beneficial Ownership Declaration](actions/get-beneficial-ownership-declaration.md) | GET |  |
| [Get Financial Report](actions/get-financial-report.md) | GET |  |
| [Get Non-Financial Report](actions/get-non-financial-report.md) | GET |  |
| [Search Documents](actions/search-documents.md) | GET |  |

### Publication

| Action | Method | Description |
| --- | --- | --- |
| [Search Publications](actions/search-publications.md) | GET |  |

