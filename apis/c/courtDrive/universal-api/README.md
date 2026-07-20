# <img src="https://images.mindcloud.co/apps/icons/court-drive_1775572288990.png" alt="Court Drive logo" width="28" height="28"> Court Drive: Universal API

Search PACER cases and retrieve dockets, claims, and parties

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/courtDrive/latest
- **Category:** Productivity / Legal & Contracts
- **Actions:** 40
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.courtapi.com
- **Vendor API docs:** https://www.courtapi.com/docs/api

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List PACER Courts](actions/list-pacer-courts.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/courtDrive/latest/actions/list-pacer-courts?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (40)

### Async Task

| Action | Method | Description |
| --- | --- | --- |
| [Get Async Request Progress](actions/get-async-request-progress.md) | GET |  |

### Async Task Result

| Action | Method | Description |
| --- | --- | --- |
| [Get Async Request Results](actions/get-async-request-results.md) | GET |  |

### Attorney

| Action | Method | Description |
| --- | --- | --- |
| [List Case Attorneys](actions/list-case-attorneys.md) | GET |  |

### Case

| Action | Method | Description |
| --- | --- | --- |
| [Get Case Root Menu](actions/get-case-root-menu.md) | GET |  |
| [Get Case Root Menu by UUID](actions/get-case-root-menu-by-uuid.md) | GET |  |
| [Search Bankruptcy Court Cases](actions/search-bankruptcy-court-cases.md) | GET |  |
| [Search Court Cases](actions/search-court-cases.md) | GET |  |
| [Search Court Cases by Number](actions/search-court-cases-by-number.md) | GET |  |
| [Search District Court Cases](actions/search-district-court-cases.md) | GET |  |
| [Search PACER Case by Number](actions/search-pacer-case-by-number.md) | GET |  |
| [Search PACER Cases by Case Title or Party Name](actions/search-pacer-cases-by-case-title-or-party-name.md) | GET |  |

### Case Header

| Action | Method | Description |
| --- | --- | --- |
| [Get Case Headers](actions/get-case-headers.md) | GET |  |

### Case History

| Action | Method | Description |
| --- | --- | --- |
| [Get Case History](actions/get-case-history.md) | GET |  |

### Case Summary

| Action | Method | Description |
| --- | --- | --- |
| [Get Case Summary](actions/get-case-summary.md) | GET |  |

### Claim

| Action | Method | Description |
| --- | --- | --- |
| [Get Case Claim](actions/get-case-claim.md) | GET |  |
| [List Case Claims](actions/list-case-claims.md) | GET |  |

### Court

| Action | Method | Description |
| --- | --- | --- |
| [Get PACER Court Details](actions/get-pacer-court-details.md) | GET |  |
| [List PACER Courts](actions/list-pacer-courts.md) | GET |  |

### Creditor

| Action | Method | Description |
| --- | --- | --- |
| [List Case Creditors](actions/list-case-creditors.md) | GET |  |

### Docket

| Action | Method | Description |
| --- | --- | --- |
| [Get Case Docket Entry](actions/get-case-docket-entry.md) | GET |  |
| [List Case Dockets](actions/list-case-dockets.md) | GET |  |

### Filer

| Action | Method | Description |
| --- | --- | --- |
| [List Case Filers](actions/list-case-filers.md) | GET |  |

### Ncl Search

| Action | Method | Description |
| --- | --- | --- |
| [Search PACER NCL All Courts Cases](actions/search-pacer-ncl-all-courts-cases.md) | GET |  |
| [Search PACER NCL Bankruptcy Cases](actions/search-pacer-ncl-bankruptcy-cases.md) | GET |  |
| [Search PACER NCL Civil Cases](actions/search-pacer-ncl-civil-cases.md) | GET |  |

### Ncl Search Result

| Action | Method | Description |
| --- | --- | --- |
| [Get PACER NCL All Courts Results](actions/get-pacer-ncl-all-courts-results.md) | GET |  |
| [Get PACER NCL Bankruptcy Results](actions/get-pacer-ncl-bankruptcy-results.md) | GET |  |
| [Get PACER NCL Civil Results](actions/get-pacer-ncl-civil-results.md) | GET |  |

### Pacer Credential

| Action | Method | Description |
| --- | --- | --- |
| [Delete PACER Credentials](actions/delete-pacer-credentials.md) | DELETE |  |
| [Get PACER Credentials](actions/get-pacer-credentials.md) | GET |  |
| [Set PACER Credentials](actions/set-pacer-credentials.md) | PUT |  |

### Pacer Credential Validation

| Action | Method | Description |
| --- | --- | --- |
| [Validate PACER Credentials](actions/validate-pacer-credentials.md) | GET |  |

### Pacer Filer Status

| Action | Method | Description |
| --- | --- | --- |
| [Check PACER Account Filer Status](actions/check-pacer-account-filer-status.md) | GET |  |

### Party

| Action | Method | Description |
| --- | --- | --- |
| [List Case Parties](actions/list-case-parties.md) | GET |  |

### Region

| Action | Method | Description |
| --- | --- | --- |
| [Get PACER Region](actions/get-pacer-region.md) | GET |  |
| [List PACER Regions](actions/list-pacer-regions.md) | GET |  |

### Trustee

| Action | Method | Description |
| --- | --- | --- |
| [List Case Trustees](actions/list-case-trustees.md) | GET |  |

### Webhook

| Action | Method | Description |
| --- | --- | --- |
| [Create Webhook](actions/create-webhook.md) | POST |  |
| [Get Webhook](actions/get-webhook.md) | GET |  |
| [List Webhooks](actions/list-webhooks.md) | GET |  |

