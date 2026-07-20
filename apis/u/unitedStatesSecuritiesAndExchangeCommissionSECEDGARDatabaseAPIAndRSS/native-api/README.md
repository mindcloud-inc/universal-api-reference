# United States Securities and Exchange Commission (SEC) EDGAR Database: Native API Reference

A consolidated summary of United States Securities and Exchange Commission (SEC) EDGAR Database's API configuration and 49 documented operations, with links to official documentation.

- **Official docs:** https://www.sec.gov/search-filings/edgar-application-programming-interfaces
- **API base URL:** `https://www.sec.gov`

## Authentication

### No Authentication

SEC public EDGAR data APIs and RSS feeds do not require authentication or API keys. Requests must still follow SEC fair-access guidance, including a declared User-Agent header.

This API does not require request authentication.

[Official authentication documentation](https://www.sec.gov/search-filings/edgar-application-programming-interfaces)

### EDGAR Filer API Token

Use this credential for EDGAR Next endpoints that require only a filer API token, such as operational status and submission status APIs.

### Credentials

- **Filer API Token:** `filerApiToken` · optional · JWT filer API token generated in EDGAR Filer Management.

[Official authentication documentation](https://api.edgarfiling.sec.gov/openapi.json)

## API conventions

Shared headers:

| Header | Value |
| --- | --- |
| `User-Agent` | `MindCloud apps@mindcloud.co` |

Responses from this API use JSON.

## Retry behavior

Retry responses with status codes `429,500,502,503,504`. Wait 1000 ms before the first retry. Stop after 2 attempts. Multiply the delay by 2 after each failed attempt.

## Endpoints (49 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Check Multiple Submission Statuses](actions/check-multiple-submission-statuses.md) | `POST https://api.edgarfiling.sec.gov/submission/status` | [docs](https://api.edgarfiling.sec.gov/openapi.json) |
| [Check Single Submission Status](actions/check-single-submission-status.md) | `GET https://api.edgarfiling.sec.gov/submission/[:accessionNumber]/status` | [docs](https://api.edgarfiling.sec.gov/openapi.json) |
| [Create Custom CCC](actions/create-custom-ccc.md) | `PUT https://api.edgarfiling.sec.gov/fm/[:cik]/ccc` | [docs](https://api.edgarfiling.sec.gov/openapi.json) |
| [Download Company Facts Bulk ZIP](actions/download-company-facts-bulk-zip.md) | `GET /Archives/edgar/daily-index/xbrl/companyfacts.zip` | [docs](https://www.sec.gov/search-filings/edgar-application-programming-interfaces) |
| [Download Feed Archive](actions/download-feed-archive.md) | `GET /Archives/edgar/Feed/[:year]/[:quarter]/[:feedDate].nc.tar.gz` | [docs](https://www.sec.gov/search-filings/edgar-search-assistance/accessing-edgar-data) |
| [Download Oldloads Archive](actions/download-oldloads-archive.md) | `GET /Archives/edgar/Oldloads/[:year]/[:quarter]/[:loadDate].gz` | [docs](https://www.sec.gov/search-filings/edgar-search-assistance/accessing-edgar-data) |
| [Download Submissions Bulk ZIP](actions/download-submissions-bulk-zip.md) | `GET /Archives/edgar/daily-index/bulkdata/submissions.zip` | [docs](https://www.sec.gov/search-filings/edgar-application-programming-interfaces) |
| [Generate CCC](actions/generate-ccc.md) | `POST https://api.edgarfiling.sec.gov/fm/[:cik]/ccc` | [docs](https://api.edgarfiling.sec.gov/openapi.json) |
| [Get CIK Lookup Data](actions/get-cik-lookup-data.md) | `GET /Archives/edgar/cik-lookup-data.txt` | [docs](https://www.sec.gov/search-filings/edgar-search-assistance/accessing-edgar-data) |
| [Get Company Concept](actions/get-company-concept.md) | `GET https://data.sec.gov/api/xbrl/companyconcept/CIK[:cik]/[:taxonomy]/[:tag].json` | [docs](https://www.sec.gov/search-filings/edgar-application-programming-interfaces) |
| [Get Company Facts](actions/get-company-facts.md) | `GET https://data.sec.gov/api/xbrl/companyfacts/CIK[:cik].json` | [docs](https://www.sec.gov/search-filings/edgar-application-programming-interfaces) |
| [Get Company Filings Atom Feed](actions/get-company-filings-atom-feed.md) | `GET /cgi-bin/browse-edgar` | [docs](https://www.sec.gov/about/rss-feeds) |
| [Get Company Submissions](actions/get-company-submissions.md) | `GET https://data.sec.gov/submissions/CIK[:cik].json` | [docs](https://www.sec.gov/search-filings/edgar-application-programming-interfaces) |
| [Get Company Submissions File](actions/get-company-submissions-file.md) | `GET https://data.sec.gov/submissions/[:fileName]` | [docs](https://www.sec.gov/search-filings/edgar-application-programming-interfaces) |
| [Get Current Full Company Index](actions/get-current-full-company-index.md) | `GET /Archives/edgar/full-index/company.idx` | [docs](https://www.sec.gov/search-filings/edgar-search-assistance/accessing-edgar-data) |
| [Get Current Full Form Index](actions/get-current-full-form-index.md) | `GET /Archives/edgar/full-index/form.idx` | [docs](https://www.sec.gov/search-filings/edgar-search-assistance/accessing-edgar-data) |
| [Get Current Full Master Index](actions/get-current-full-master-index.md) | `GET /Archives/edgar/full-index/master.idx` | [docs](https://www.sec.gov/search-filings/edgar-search-assistance/accessing-edgar-data) |
| [Get Current Full XBRL Index](actions/get-current-full-xbrl-index.md) | `GET /Archives/edgar/full-index/xbrl.idx` | [docs](https://www.sec.gov/search-filings/edgar-search-assistance/accessing-edgar-data) |
| [Get Daily Company Index](actions/get-daily-company-index.md) | `GET /Archives/edgar/daily-index/[:year]/[:quarter]/company.[:date].idx` | [docs](https://www.sec.gov/search-filings/edgar-search-assistance/accessing-edgar-data) |
| [Get Daily Form Index](actions/get-daily-form-index.md) | `GET /Archives/edgar/daily-index/[:year]/[:quarter]/form.[:date].idx` | [docs](https://www.sec.gov/search-filings/edgar-search-assistance/accessing-edgar-data) |
| [Get Daily Master Index](actions/get-daily-master-index.md) | `GET /Archives/edgar/daily-index/[:year]/[:quarter]/master.[:date].idx` | [docs](https://www.sec.gov/search-filings/edgar-search-assistance/accessing-edgar-data) |
| [Get Daily XBRL Index](actions/get-daily-xbrl-index.md) | `GET /Archives/edgar/daily-index/xbrl/[:year]/[:quarter]/xbrl.[:date].idx` | [docs](https://www.sec.gov/search-filings/edgar-search-assistance/accessing-edgar-data) |
| [Get Delegations](actions/get-delegations.md) | `GET https://api.edgarfiling.sec.gov/fm/[:cik]/delegations` | [docs](https://api.edgarfiling.sec.gov/openapi.json) |
| [Get EDGAR Operational Status](actions/get-edgar-operational-status.md) | `GET https://api.edgarfiling.sec.gov/status` | [docs](https://api.edgarfiling.sec.gov/openapi.json) |
| [Get Filer Account Information](actions/get-filer-account-information.md) | `GET https://api.edgarfiling.sec.gov/fm/[:cik]` | [docs](https://api.edgarfiling.sec.gov/openapi.json) |
| [Get Filing Document](actions/get-filing-document.md) | `GET /Archives/edgar/data/[:cik]/[:accessionNumberNoDashes]/[:documentName]` | [docs](https://www.sec.gov/search-filings/edgar-search-assistance/accessing-edgar-data) |
| [Get Filing Index Page](actions/get-filing-index-page.md) | `GET /Archives/edgar/data/[:cik]/[:accessionNumberNoDashes]/[:accessionNumber]-index.html` | [docs](https://www.sec.gov/search-filings/edgar-search-assistance/accessing-edgar-data) |
| [Get Filing Text](actions/get-filing-text.md) | `GET /Archives/edgar/data/[:cik]/[:accessionNumber].txt` | [docs](https://www.sec.gov/search-filings/edgar-search-assistance/accessing-edgar-data) |
| [Get Individuals](actions/get-individuals.md) | `GET https://api.edgarfiling.sec.gov/fm/[:cik]/individuals` | [docs](https://api.edgarfiling.sec.gov/openapi.json) |
| [Get Latest Filings Atom Feed](actions/get-latest-filings-atom-feed.md) | `GET /cgi-bin/browse-edgar` | [docs](https://www.sec.gov/about/rss-feeds) |
| [Get Quarterly Company Index](actions/get-quarterly-company-index.md) | `GET /Archives/edgar/full-index/[:year]/[:quarter]/company.idx` | [docs](https://www.sec.gov/search-filings/edgar-search-assistance/accessing-edgar-data) |
| [Get Quarterly Form Index](actions/get-quarterly-form-index.md) | `GET /Archives/edgar/full-index/[:year]/[:quarter]/form.idx` | [docs](https://www.sec.gov/search-filings/edgar-search-assistance/accessing-edgar-data) |
| [Get Quarterly Master Index](actions/get-quarterly-master-index.md) | `GET /Archives/edgar/full-index/[:year]/[:quarter]/master.idx` | [docs](https://www.sec.gov/search-filings/edgar-search-assistance/accessing-edgar-data) |
| [Get Quarterly XBRL Index](actions/get-quarterly-xbrl-index.md) | `GET /Archives/edgar/full-index/[:year]/[:quarter]/xbrl.idx` | [docs](https://www.sec.gov/search-filings/edgar-search-assistance/accessing-edgar-data) |
| [Get Structured Disclosure Monthly RSS Archive](actions/get-structured-disclosure-monthly-rss-archive.md) | `GET /Archives/edgar/monthly/xbrlrss-[:yearMonth].xml` | [docs](https://www.sec.gov/data-research/structured-data/structured-disclosure-rss-feeds) |
| [Get XBRL Frame](actions/get-xbrl-frame.md) | `GET https://data.sec.gov/api/xbrl/frames/[:taxonomy]/[:tag]/[:unit]/[:period].json` | [docs](https://www.sec.gov/search-filings/edgar-application-programming-interfaces) |
| [List Company Tickers](actions/list-company-tickers.md) | `GET /files/company_tickers.json` | [docs](https://www.sec.gov/search-filings/edgar-search-assistance/accessing-edgar-data) |
| [List Company Tickers By Exchange](actions/list-company-tickers-by-exchange.md) | `GET /files/company_tickers_exchange.json` | [docs](https://www.sec.gov/search-filings/edgar-search-assistance/accessing-edgar-data) |
| [List Daily Bulk Data Directory](actions/list-daily-bulk-data-directory.md) | `GET /Archives/edgar/daily-index/bulkdata/index.json` | [docs](https://www.sec.gov/search-filings/edgar-search-assistance/accessing-edgar-data) |
| [List Daily Index Directory](actions/list-daily-index-directory.md) | `GET /Archives/edgar/daily-index/[:year]/[:quarter]/index.json` | [docs](https://www.sec.gov/search-filings/edgar-search-assistance/accessing-edgar-data) |
| [List Daily Index Root Directory](actions/list-daily-index-root-directory.md) | `GET /Archives/edgar/daily-index/index.json` | [docs](https://www.sec.gov/search-filings/edgar-search-assistance/accessing-edgar-data) |
| [List Daily XBRL Bulk Directory](actions/list-daily-xbrl-bulk-directory.md) | `GET /Archives/edgar/daily-index/xbrl/index.json` | [docs](https://www.sec.gov/search-filings/edgar-search-assistance/accessing-edgar-data) |
| [List Feed Directory](actions/list-feed-directory.md) | `GET /Archives/edgar/Feed/[:year]/[:quarter]/index.json` | [docs](https://www.sec.gov/search-filings/edgar-search-assistance/accessing-edgar-data) |
| [List Feed Root Directory](actions/list-feed-root-directory.md) | `GET /Archives/edgar/Feed/index.json` | [docs](https://www.sec.gov/search-filings/edgar-search-assistance/accessing-edgar-data) |
| [List Full Index Directory](actions/list-full-index-directory.md) | `GET /Archives/edgar/full-index/index.json` | [docs](https://www.sec.gov/search-filings/edgar-search-assistance/accessing-edgar-data) |
| [List Mutual Fund Tickers](actions/list-mutual-fund-tickers.md) | `GET /files/company_tickers_mf.json` | [docs](https://www.sec.gov/search-filings/edgar-search-assistance/accessing-edgar-data) |
| [List Oldloads Directory](actions/list-oldloads-directory.md) | `GET /Archives/edgar/Oldloads/[:year]/[:quarter]/index.json` | [docs](https://www.sec.gov/search-filings/edgar-search-assistance/accessing-edgar-data) |
| [List Oldloads Root Directory](actions/list-oldloads-root-directory.md) | `GET /Archives/edgar/Oldloads/index.json` | [docs](https://www.sec.gov/search-filings/edgar-search-assistance/accessing-edgar-data) |
| [Verify Filing Credentials](actions/verify-filing-credentials.md) | `GET https://api.edgarfiling.sec.gov/fm/[:cik]/verify` | [docs](https://api.edgarfiling.sec.gov/openapi.json) |
