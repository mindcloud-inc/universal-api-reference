# Court Drive: Native API Reference

A consolidated summary of Court Drive's API configuration and 40 documented operations, with links to official documentation.

- **Official docs:** https://www.courtapi.com/docs/api
- **OpenAPI specification:** https://www.courtapi.com/swagger/spec/courtapi-oas3.json
- **API base URL:** `https://v1.courtapi.com`

## Authentication

### Basic Auth

Use your CourtAPI app_id as Username and app_key as Password.

### Credentials

- **Username:** `username` · required
- **Password:** `password` · required

Join the username and password with a colon, Base64-encode the result, and send it with the `Basic` authorization scheme:

```js
const credentials = Buffer.from(`${username}:${password}`).toString('base64');

const response = await fetch(url, {
  headers: {
    Authorization: `Basic ${credentials}`
  }
});
```

[Official authentication documentation](https://www.courtapi.com/docs/playground)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Endpoints (40 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Check PACER Account Filer Status](actions/check-pacer-account-filer-status.md) | `POST /pacer/credentials/check-filer-status` | [docs](https://www.courtapi.com/docs/playground) |
| [Create Webhook](actions/create-webhook.md) | `POST /webhooks` | [docs](https://www.courtapi.com/docs/playground) |
| [Delete PACER Credentials](actions/delete-pacer-credentials.md) | `DELETE /pacer/credentials` | [docs](https://www.courtapi.com/docs/playground) |
| [Get Async Request Progress](actions/get-async-request-progress.md) | `GET /progress/{task_id}` | [docs](https://www.courtapi.com/docs/playground) |
| [Get Async Request Results](actions/get-async-request-results.md) | `GET /async/{task_id}/results` | [docs](https://www.courtapi.com/docs/playground) |
| [Get Case Claim](actions/get-case-claim.md) | `GET /cases/pacer/{court_code}/{case_number}/claims/{claim_no}` | [docs](https://www.courtapi.com/docs/playground) |
| [Get Case Docket Entry](actions/get-case-docket-entry.md) | `GET /cases/pacer/{court_code}/{case_number}/dockets/{docket_no}` | [docs](https://www.courtapi.com/docs/playground) |
| [Get Case Headers](actions/get-case-headers.md) | `GET /cases/pacer/{court_code}/{case_number}/headers` | [docs](https://www.courtapi.com/docs/playground) |
| [Get Case History](actions/get-case-history.md) | `GET /cases/pacer/{court_code}/{case_number}/history` | [docs](https://www.courtapi.com/docs/playground) |
| [Get Case Root Menu](actions/get-case-root-menu.md) | `GET /cases/pacer/{court_code}/{case_number}` | [docs](https://www.courtapi.com/docs/playground) |
| [Get Case Root Menu by UUID](actions/get-case-root-menu-by-uuid.md) | `GET /cases/pacer/by-uuid/{case_uuid}` | [docs](https://www.courtapi.com/docs/playground) |
| [Get Case Summary](actions/get-case-summary.md) | `GET /cases/pacer/{court_code}/{case_number}/case_summary` | [docs](https://www.courtapi.com/docs/playground) |
| [Get PACER Court Details](actions/get-pacer-court-details.md) | `GET /courts/pacer/{court_code}` | [docs](https://www.courtapi.com/docs/playground) |
| [Get PACER Credentials](actions/get-pacer-credentials.md) | `GET /pacer/credentials` | [docs](https://www.courtapi.com/docs/playground) |
| [Get PACER NCL All Courts Results](actions/get-pacer-ncl-all-courts-results.md) | `GET /pacer/ncl/all/{search_id}` | [docs](https://www.courtapi.com/docs/playground) |
| [Get PACER NCL Bankruptcy Results](actions/get-pacer-ncl-bankruptcy-results.md) | `GET /pacer/ncl/bankruptcy/{search_id}` | [docs](https://www.courtapi.com/docs/playground) |
| [Get PACER NCL Civil Results](actions/get-pacer-ncl-civil-results.md) | `GET /pacer/ncl/civil/{search_id}` | [docs](https://www.courtapi.com/docs/playground) |
| [Get PACER Region](actions/get-pacer-region.md) | `GET /regions/pacer/{region_code}` | [docs](https://www.courtapi.com/docs/playground) |
| [Get Webhook](actions/get-webhook.md) | `GET /webhooks/{webhook_id}` | [docs](https://www.courtapi.com/docs/playground) |
| [List Case Attorneys](actions/list-case-attorneys.md) | `GET /cases/pacer/{court_code}/{case_number}/attorneys` | [docs](https://www.courtapi.com/docs/playground) |
| [List Case Claims](actions/list-case-claims.md) | `GET /cases/pacer/{court_code}/{case_number}/claims` | [docs](https://www.courtapi.com/docs/playground) |
| [List Case Creditors](actions/list-case-creditors.md) | `GET /cases/pacer/{court_code}/{case_number}/creditors` | [docs](https://www.courtapi.com/docs/playground) |
| [List Case Dockets](actions/list-case-dockets.md) | `GET /cases/pacer/{court_code}/{case_number}/dockets` | [docs](https://www.courtapi.com/docs/playground) |
| [List Case Filers](actions/list-case-filers.md) | `GET /cases/pacer/{court_code}/{case_number}/filers` | [docs](https://www.courtapi.com/docs/playground) |
| [List Case Parties](actions/list-case-parties.md) | `GET /cases/pacer/{court_code}/{case_number}/parties` | [docs](https://www.courtapi.com/docs/playground) |
| [List Case Trustees](actions/list-case-trustees.md) | `GET /cases/pacer/{court_code}/{case_number}/trustees` | [docs](https://www.courtapi.com/docs/playground) |
| [List PACER Courts](actions/list-pacer-courts.md) | `GET /courts/pacer` | [docs](https://www.courtapi.com/docs/playground) |
| [List PACER Regions](actions/list-pacer-regions.md) | `GET /regions/pacer` | [docs](https://www.courtapi.com/docs/playground) |
| [List Webhooks](actions/list-webhooks.md) | `GET /webhooks` | [docs](https://www.courtapi.com/docs/playground) |
| [Search Bankruptcy Court Cases](actions/search-bankruptcy-court-cases.md) | `POST /courts/pacer/{court_code}/cases/search/bankruptcy` | [docs](https://www.courtapi.com/docs/playground) |
| [Search Court Cases](actions/search-court-cases.md) | `POST /courts/pacer/{court_code}/cases/search` | [docs](https://www.courtapi.com/docs/playground) |
| [Search Court Cases by Number](actions/search-court-cases-by-number.md) | `POST /courts/pacer/{court_code}/cases/search/by-case-number` | [docs](https://www.courtapi.com/docs/playground) |
| [Search District Court Cases](actions/search-district-court-cases.md) | `POST /courts/pacer/{court_code}/cases/search/district` | [docs](https://www.courtapi.com/docs/playground) |
| [Search PACER Case by Number](actions/search-pacer-case-by-number.md) | `GET /cases/pacer/search/case_no/{case_number}` | [docs](https://www.courtapi.com/docs/playground) |
| [Search PACER Cases by Case Title or Party Name](actions/search-pacer-cases-by-case-title-or-party-name.md) | `GET /cases/pacer/search/party_title` | [docs](https://www.courtapi.com/docs/playground) |
| [Search PACER NCL All Courts Cases](actions/search-pacer-ncl-all-courts-cases.md) | `POST /pacer/ncl/all` | [docs](https://www.courtapi.com/docs/playground) |
| [Search PACER NCL Bankruptcy Cases](actions/search-pacer-ncl-bankruptcy-cases.md) | `POST /pacer/ncl/bankruptcy` | [docs](https://www.courtapi.com/docs/playground) |
| [Search PACER NCL Civil Cases](actions/search-pacer-ncl-civil-cases.md) | `POST /pacer/ncl/civil` | [docs](https://www.courtapi.com/docs/playground) |
| [Set PACER Credentials](actions/set-pacer-credentials.md) | `POST /pacer/credentials` | [docs](https://www.courtapi.com/docs/playground) |
| [Validate PACER Credentials](actions/validate-pacer-credentials.md) | `POST /pacer/credentials/validate` | [docs](https://www.courtapi.com/docs/playground) |
