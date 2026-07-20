# <img src="https://images.mindcloud.co/apps/icons/seal-of-the-united-states-securities-and-exchange-commission_1776372935261.png" alt="United States Securities and Exchange Commission (SEC) EDGAR Database logo" width="28" height="28"> United States Securities and Exchange Commission (SEC) EDGAR Database: Universal API

Access public SEC EDGAR company submissions, XBRL financial data, ticker/CIK association files, archive indexes, filing documents, and RSS/Atom filing feeds.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/unitedStatesSecuritiesAndExchangeCommissionSECEDGARDatabaseAPIAndRSS/latest
- **Actions:** 49
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.sec.gov/
- **Vendor API docs:** https://www.sec.gov/search-filings/edgar-application-programming-interfaces

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Company Tickers](actions/list-company-tickers.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/unitedStatesSecuritiesAndExchangeCommissionSECEDGARDatabaseAPIAndRSS/latest/actions/list-company-tickers?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (49)

### Companies

| Action | Method | Description |
| --- | --- | --- |
| [Get CIK Lookup Data](actions/get-cik-lookup-data.md) | GET | Retrieves the EDGAR CIK lookup text file. |
| [Get Company Submissions](actions/get-company-submissions.md) | GET | Retrieves company submission history from SEC EDGAR. |
| [Get Company Submissions File](actions/get-company-submissions-file.md) | GET | Retrieves a company submissions file from SEC EDGAR. |
| [Get Filer Account Information](actions/get-filer-account-information.md) | GET | Retrieves filer account information from the EDGAR API. |
| [List Company Tickers](actions/list-company-tickers.md) | GET | Retrieves company ticker mappings from SEC EDGAR. |
| [List Company Tickers By Exchange](actions/list-company-tickers-by-exchange.md) | GET | Retrieves company ticker mappings by exchange from SEC EDGAR. |
| [List Mutual Fund Tickers](actions/list-mutual-fund-tickers.md) | GET | Retrieves mutual fund ticker mappings from SEC EDGAR. |

### Connections

| Action | Method | Description |
| --- | --- | --- |
| [Create Custom CCC](actions/create-custom-ccc.md) | PUT | Updates a filer's CCC to a custom value in EDGAR. |
| [Generate CCC](actions/generate-ccc.md) | PUT | Updates a filer's CCC with a generated value in EDGAR. |
| [Get Delegations](actions/get-delegations.md) | GET | Retrieves delegation relationships for an EDGAR filer account. |
| [Verify Filing Credentials](actions/verify-filing-credentials.md) | GET | Retrieves filing credential verification results from the EDGAR API. |

### Documents

| Action | Method | Description |
| --- | --- | --- |
| [Get Company Filings Atom Feed](actions/get-company-filings-atom-feed.md) | GET | Retrieves a company filings Atom feed from SEC EDGAR. |
| [Get Current Full Company Index](actions/get-current-full-company-index.md) | GET | Retrieves the current SEC EDGAR full company index. |
| [Get Current Full Form Index](actions/get-current-full-form-index.md) | GET | Retrieves the current SEC EDGAR full form index. |
| [Get Current Full Master Index](actions/get-current-full-master-index.md) | GET | Retrieves the current SEC EDGAR full master index. |
| [Get Current Full XBRL Index](actions/get-current-full-xbrl-index.md) | GET | Retrieves the current SEC EDGAR full XBRL index. |
| [Get Daily Company Index](actions/get-daily-company-index.md) | GET | Retrieves the SEC EDGAR daily company index file. |
| [Get Daily Form Index](actions/get-daily-form-index.md) | GET | Retrieves the SEC EDGAR daily form index file. |
| [Get Daily Master Index](actions/get-daily-master-index.md) | GET | Retrieves the SEC EDGAR daily master index file. |
| [Get Daily XBRL Index](actions/get-daily-xbrl-index.md) | GET | Retrieves the SEC EDGAR daily XBRL index file. |
| [Get Filing Document](actions/get-filing-document.md) | GET | Retrieves a filing document from the SEC EDGAR archive. |
| [Get Filing Index Page](actions/get-filing-index-page.md) | GET | Retrieves a filing index page from SEC EDGAR. |
| [Get Filing Text](actions/get-filing-text.md) | GET | Retrieves a raw SEC EDGAR filing text file. |
| [Get Latest Filings Atom Feed](actions/get-latest-filings-atom-feed.md) | GET | Retrieves the latest filings Atom feed from SEC EDGAR. |
| [Get Quarterly Company Index](actions/get-quarterly-company-index.md) | GET | Retrieves the SEC EDGAR quarterly company index file. |
| [Get Quarterly Form Index](actions/get-quarterly-form-index.md) | GET | Retrieves the SEC EDGAR quarterly form index file. |
| [Get Quarterly Master Index](actions/get-quarterly-master-index.md) | GET | Retrieves the SEC EDGAR quarterly master index file. |
| [Get Quarterly XBRL Index](actions/get-quarterly-xbrl-index.md) | GET | Retrieves the SEC EDGAR quarterly XBRL index file. |
| [Get Structured Disclosure Monthly RSS Archive](actions/get-structured-disclosure-monthly-rss-archive.md) | GET | Retrieves a monthly structured disclosure RSS archive from SEC EDGAR. |
| [List Daily Bulk Data Directory](actions/list-daily-bulk-data-directory.md) | GET | Retrieves the SEC EDGAR bulk data directory listing. |
| [List Daily Index Directory](actions/list-daily-index-directory.md) | GET | Retrieves the SEC EDGAR daily index directory listing. |
| [List Daily Index Root Directory](actions/list-daily-index-root-directory.md) | GET | Retrieves the SEC EDGAR daily index root listing. |
| [List Daily XBRL Bulk Directory](actions/list-daily-xbrl-bulk-directory.md) | GET | Retrieves the SEC EDGAR XBRL bulk directory listing. |
| [List Feed Directory](actions/list-feed-directory.md) | GET | Retrieves the SEC EDGAR quarterly feed directory listing. |
| [List Feed Root Directory](actions/list-feed-root-directory.md) | GET | Retrieves the SEC EDGAR feed root directory listing. |
| [List Full Index Directory](actions/list-full-index-directory.md) | GET | Retrieves the SEC EDGAR full index directory listing. |
| [List Oldloads Directory](actions/list-oldloads-directory.md) | GET | Retrieves the SEC EDGAR quarterly oldloads directory listing. |
| [List Oldloads Root Directory](actions/list-oldloads-root-directory.md) | GET | Retrieves the SEC EDGAR oldloads root directory listing. |

### Files

| Action | Method | Description |
| --- | --- | --- |
| [Check Multiple Submission Statuses](actions/check-multiple-submission-statuses.md) | GET | Retrieves statuses for multiple EDGAR submissions. |
| [Check Single Submission Status](actions/check-single-submission-status.md) | GET | Retrieves the status of a single EDGAR submission. |
| [Download Company Facts Bulk ZIP](actions/download-company-facts-bulk-zip.md) | GET | Downloads the company facts bulk ZIP from SEC EDGAR. |
| [Download Feed Archive](actions/download-feed-archive.md) | GET | Downloads a daily SEC EDGAR feed archive. |
| [Download Oldloads Archive](actions/download-oldloads-archive.md) | GET | Downloads a daily SEC EDGAR oldloads archive. |
| [Download Submissions Bulk ZIP](actions/download-submissions-bulk-zip.md) | GET | Downloads the submissions bulk ZIP from SEC EDGAR. |

### Monitors

| Action | Method | Description |
| --- | --- | --- |
| [Get EDGAR Operational Status](actions/get-edgar-operational-status.md) | GET | Retrieves the current EDGAR operational status. |

### Reports

| Action | Method | Description |
| --- | --- | --- |
| [Get Company Concept](actions/get-company-concept.md) | GET | Retrieves company concept facts from SEC EDGAR. |
| [Get Company Facts](actions/get-company-facts.md) | GET | Retrieves company XBRL facts from SEC EDGAR. |
| [Get XBRL Frame](actions/get-xbrl-frame.md) | GET | Retrieves XBRL frame data from SEC EDGAR. |

### Users

| Action | Method | Description |
| --- | --- | --- |
| [Get Individuals](actions/get-individuals.md) | GET | Retrieves filer-associated individuals from the EDGAR API. |

