# <img src="https://images.mindcloud.co/apps/icons/open-fec_1777644135628.png" alt="OpenFEC logo" width="28" height="28"> OpenFEC: Universal API

Explore Federal Election Commission campaign finance data, including candidates, committees, filings, receipts, disbursements, reports, elections, and legal records.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/openFEC/latest
- **Actions:** 28
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.fec.gov/
- **Vendor API docs:** https://api.open.fec.gov/developers/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Candidates](actions/list-candidates.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/openFEC/latest/actions/list-candidates?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (28)

### Calendar Date

| Action | Method | Description |
| --- | --- | --- |
| [List Calendar Dates](actions/list-calendar-dates.md) | GET | Retrieves calendar dates from OpenFEC. |

### Candidate

| Action | Method | Description |
| --- | --- | --- |
| [Get Candidate](actions/get-candidate.md) | GET | Retrieves a candidate from OpenFEC. |
| [List Candidates](actions/list-candidates.md) | GET | Retrieves a list of candidates from OpenFEC. |

### Candidate Filing

| Action | Method | Description |
| --- | --- | --- |
| [List Candidate Filings](actions/list-candidate-filings.md) | GET | Retrieves a candidate's filings from OpenFEC. |

### Candidate History

| Action | Method | Description |
| --- | --- | --- |
| [List Candidate History](actions/list-candidate-history.md) | GET | Retrieves a candidate's history from OpenFEC. |

### Candidate Name Result

| Action | Method | Description |
| --- | --- | --- |
| [Find Candidate Names](actions/find-candidate-names.md) | GET | Finds candidate names in OpenFEC. |

### Candidate Search Result

| Action | Method | Description |
| --- | --- | --- |
| [Search Candidates](actions/search-candidates.md) | GET | Finds candidates in OpenFEC by search terms. |

### Candidate Total

| Action | Method | Description |
| --- | --- | --- |
| [List Candidate Totals](actions/list-candidate-totals.md) | GET | Retrieves a candidate's financial totals from OpenFEC. |

### Committee

| Action | Method | Description |
| --- | --- | --- |
| [Get Committee](actions/get-committee.md) | GET | Retrieves a committee from OpenFEC. |
| [List Committees](actions/list-committees.md) | GET | Retrieves a list of committees from OpenFEC. |

### Committee History

| Action | Method | Description |
| --- | --- | --- |
| [List Committee History](actions/list-committee-history.md) | GET | Retrieves a committee's history from OpenFEC. |

### Committee Name Result

| Action | Method | Description |
| --- | --- | --- |
| [Find Committee Names](actions/find-committee-names.md) | GET | Finds committee names in OpenFEC. |

### Committee Report

| Action | Method | Description |
| --- | --- | --- |
| [List Committee Reports](actions/list-committee-reports.md) | GET | Retrieves committee reports from OpenFEC. |

### Committee Total

| Action | Method | Description |
| --- | --- | --- |
| [List Committee Totals](actions/list-committee-totals.md) | GET | Retrieves committee financial totals from OpenFEC. |

### Disbursement

| Action | Method | Description |
| --- | --- | --- |
| [Get Disbursement](actions/get-disbursement.md) | GET | Retrieves a disbursement from OpenFEC. |
| [List Disbursements](actions/list-disbursements.md) | GET | Retrieves disbursements from OpenFEC. |

### Disbursement Recipient Aggregate

| Action | Method | Description |
| --- | --- | --- |
| [List Disbursements By Recipient](actions/list-disbursements-by-recipient.md) | GET | Retrieves disbursement totals in OpenFEC by recipient. |

### Election

| Action | Method | Description |
| --- | --- | --- |
| [Search Elections](actions/search-elections.md) | GET | Finds elections in OpenFEC by cycle, office, state, or district. |

### Election Summary

| Action | Method | Description |
| --- | --- | --- |
| [Get Election Summary](actions/get-election-summary.md) | GET | Retrieves an election summary from OpenFEC. |

### Filing

| Action | Method | Description |
| --- | --- | --- |
| [List Filings](actions/list-filings.md) | GET | Retrieves a list of filings from OpenFEC. |

### Independent Expenditure

| Action | Method | Description |
| --- | --- | --- |
| [List Independent Expenditures](actions/list-independent-expenditures.md) | GET | Retrieves independent expenditures from OpenFEC. |

### Itemized Receipt

| Action | Method | Description |
| --- | --- | --- |
| [Get Itemized Receipt](actions/get-itemized-receipt.md) | GET | Retrieves an itemized receipt from OpenFEC. |
| [List Itemized Receipts](actions/list-itemized-receipts.md) | GET | Retrieves itemized receipts from OpenFEC. |

### Legal Document

| Action | Method | Description |
| --- | --- | --- |
| [Search Legal Documents](actions/search-legal-documents.md) | GET | Finds legal documents in OpenFEC by search terms. |

### Receipt Employer Aggregate

| Action | Method | Description |
| --- | --- | --- |
| [List Receipts By Employer](actions/list-receipts-by-employer.md) | GET | Retrieves receipt totals in OpenFEC by employer. |

### Receipt Occupation Aggregate

| Action | Method | Description |
| --- | --- | --- |
| [List Receipts By Occupation](actions/list-receipts-by-occupation.md) | GET | Retrieves receipt totals in OpenFEC by occupation. |

### Receipt State Aggregate

| Action | Method | Description |
| --- | --- | --- |
| [List Receipts By State](actions/list-receipts-by-state.md) | GET | Retrieves receipt totals in OpenFEC by state. |

### Report

| Action | Method | Description |
| --- | --- | --- |
| [List Reports By Entity Type](actions/list-reports-by-entity-type.md) | GET | Retrieves reports in OpenFEC by entity type. |

