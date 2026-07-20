# <img src="https://images.mindcloud.co/apps/icons/lasso-x-icon_1777484391075.jpeg" alt="Lasso X logo" width="28" height="28"> Lasso X: Universal API

Retrieve company, person, production unit, registry, reporting, list, and monitoring data from Lasso X APIs for Danish CVR and related business datasets.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/lassoX/latest
- **Actions:** 24
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.lassox.com
- **Vendor API docs:** https://docs.lassox.com/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Reporting Batches](actions/list-reporting-batches.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/lassoX/latest/actions/list-reporting-batches?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (24)

### Company Delta

| Action | Method | Description |
| --- | --- | --- |
| [List Company Delta](actions/list-company-delta.md) | GET | Retrieves changed companies from Lasso X since a given date. |

### Creditsafe Rating

| Action | Method | Description |
| --- | --- | --- |
| [Get CreditSafe Rating](actions/get-creditsafe-rating.md) | GET | Retrieves a CreditSafe rating from Lasso X by CVR number. |

### Cvr Entity

| Action | Method | Description |
| --- | --- | --- |
| [Get CVR Entity](actions/get-cvr-entity.md) | GET | Retrieves a CVR entity from Lasso X by Lasso ID. |

### Cvr Entity History

| Action | Method | Description |
| --- | --- | --- |
| [Get CVR Entity History](actions/get-cvr-entity-history.md) | GET | Retrieves CVR entity history from Lasso X by Lasso ID. |

### Cvr Search Results

| Action | Method | Description |
| --- | --- | --- |
| [Search CVR](actions/search-cvr.md) | GET | Finds CVR companies or people in Lasso X by query. |

### Financial Analysis

| Action | Method | Description |
| --- | --- | --- |
| [Analyze Financial Report](actions/analyze-financial-report.md) | GET | Retrieves a financial report analysis from Lasso X. |

### Latest Report

| Action | Method | Description |
| --- | --- | --- |
| [Get Latest Report](actions/get-latest-report.md) | GET | Retrieves the latest report for a CVR entity from Lasso X. |

### Latest Report Pdf

| Action | Method | Description |
| --- | --- | --- |
| [Download Latest Report PDF](actions/download-latest-report-pdf.md) | GET | Retrieves the latest report file for a CVR entity from Lasso X. |

### Network

| Action | Method | Description |
| --- | --- | --- |
| [Get Network](actions/get-network.md) | GET | Retrieves a person's professional network from Lasso X. |

### Paqle Entity

| Action | Method | Description |
| --- | --- | --- |
| [Get Paqle Entity](actions/get-paqle-entity.md) | GET | Retrieves Paqle entity details from Lasso X by Lasso ID. |

### Paqle News

| Action | Method | Description |
| --- | --- | --- |
| [List Paqle News](actions/list-paqle-news.md) | GET | Retrieves Paqle news for a Lasso X entity. |

### Person Delta

| Action | Method | Description |
| --- | --- | --- |
| [List Person Delta](actions/list-person-delta.md) | GET | Retrieves changed people from Lasso X since a given date. |

### Phone Number Lookup

| Action | Method | Description |
| --- | --- | --- |
| [Lookup Phone Number](actions/lookup-phone-number.md) | GET | Finds a phone number in Lasso X by number. |

### Phone Numbers

| Action | Method | Description |
| --- | --- | --- |
| [List Phone Numbers](actions/list-phone-numbers.md) | GET | Retrieves phone numbers for a Lasso X entity. |

### Production Unit Delta

| Action | Method | Description |
| --- | --- | --- |
| [List Production Unit Delta](actions/list-production-unit-delta.md) | GET | Retrieves changed production units from Lasso X since a given date. |

### Property Summary

| Action | Method | Description |
| --- | --- | --- |
| [Get Property Summary](actions/get-property-summary.md) | GET | Retrieves a property summary from Lasso X. |

### Related People

| Action | Method | Description |
| --- | --- | --- |
| [Get Related People](actions/get-related-people.md) | GET | Retrieves related people for a CVR entity from Lasso X. |

### Related People History

| Action | Method | Description |
| --- | --- | --- |
| [Get Related People History](actions/get-related-people-history.md) | GET | Retrieves related people history for a CVR entity from Lasso X. |

### Report Delta

| Action | Method | Description |
| --- | --- | --- |
| [List Report Delta](actions/list-report-delta.md) | GET | Retrieves changed reports from Lasso X since a given date. |

### Reporting Batch

| Action | Method | Description |
| --- | --- | --- |
| [Create Reporting Batch](actions/create-reporting-batch.md) | POST | Creates a reporting batch in Lasso X. |
| [Get Reporting Batch](actions/get-reporting-batch.md) | GET | Retrieves a reporting batch from Lasso X by ID. |

### Reporting Batch Items

| Action | Method | Description |
| --- | --- | --- |
| [List Reporting Batch Items](actions/list-reporting-batch-items.md) | GET | Retrieves items for a reporting batch from Lasso X. |

### Reporting Batches

| Action | Method | Description |
| --- | --- | --- |
| [List Reporting Batches](actions/list-reporting-batches.md) | GET | Retrieves reporting batches from Lasso X. |

### Reports

| Action | Method | Description |
| --- | --- | --- |
| [List Reports](actions/list-reports.md) | GET | Retrieves reports for a CVR entity from Lasso X. |

