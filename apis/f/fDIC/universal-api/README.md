# <img src="https://images.mindcloud.co/apps/icons/favicon-api-fdic-gov-48x48_1777483792790.png" alt="FDIC logo" width="28" height="28"> FDIC: Universal API

Access FDIC BankFind Suite public banking data for insured institutions, branch locations, structure history, financials, summary data, failures, Summary of Deposits, and demographics.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/fDIC/latest
- **Actions:** 8
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.fdic.gov/resources/data-tools/
- **Vendor API docs:** https://api.fdic.gov/banks/docs

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Bank Failures](actions/list-bank-failures.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/fDIC/latest/actions/list-bank-failures?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (8)

### Bank Failure

| Action | Method | Description |
| --- | --- | --- |
| [List Bank Failures](actions/list-bank-failures.md) | GET | Retrieves failed bank records from FDIC. |

### Demographics Summary

| Action | Method | Description |
| --- | --- | --- |
| [List Demographics Summary](actions/list-demographics-summary.md) | GET | Retrieves demographic banking data from FDIC. |

### Financial Institution

| Action | Method | Description |
| --- | --- | --- |
| [List Financial Institutions](actions/list-financial-institutions.md) | GET | Retrieves financial institutions from FDIC. |

### Historical Aggregate Data

| Action | Method | Description |
| --- | --- | --- |
| [List Historical Aggregate Data](actions/list-historical-aggregate-data.md) | GET | Retrieves historical aggregate banking data from FDIC. |

### Institution Financial

| Action | Method | Description |
| --- | --- | --- |
| [List Institution Financials](actions/list-institution-financials.md) | GET | Retrieves institution financial data from FDIC. |

### Institution Location

| Action | Method | Description |
| --- | --- | --- |
| [List Institution Locations](actions/list-institution-locations.md) | GET | Retrieves institution locations from FDIC. |

### Structure Change Event

| Action | Method | Description |
| --- | --- | --- |
| [List Structure Change Events](actions/list-structure-change-events.md) | GET | Retrieves structure change events from FDIC. |

### Summary Of Deposits

| Action | Method | Description |
| --- | --- | --- |
| [List Summary Of Deposits](actions/list-summary-of-deposits.md) | GET | Retrieves summary of deposits data from FDIC. |

