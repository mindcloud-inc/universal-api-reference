# <img src="https://images.mindcloud.co/apps/icons/zero-bounce_1773328405541.png" alt="ZeroBounce logo" width="28" height="28"> ZeroBounce: Universal API

ZeroBounce: validate emails, find contacts, score addresses, and run bulk email quality workflows.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/zeroBounce/latest
- **Category:** Marketing
- **Actions:** 18
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.zerobounce.net
- **Vendor API docs:** https://www.zerobounce.net/docs

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Credit Balance](actions/get-credit-balance.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/zeroBounce/latest/actions/get-credit-balance?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (18)

### Account

| Action | Method | Description |
| --- | --- | --- |
| [Get API Usage](actions/get-api-usage.md) | GET | Retrieves API usage metrics from ZeroBounce by date range. |
| [Get Credit Balance](actions/get-credit-balance.md) | GET | Retrieves credit balance details from ZeroBounce. |

### Activity Data

| Action | Method | Description |
| --- | --- | --- |
| [Get Activity Data](actions/get-activity-data.md) | GET | Retrieves activity data for an email from ZeroBounce. |

### Contacts

| Action | Method | Description |
| --- | --- | --- |
| [Find Email](actions/find-email.md) | GET | Finds contact emails in ZeroBounce by domain or company. |

### Domain Search

| Action | Method | Description |
| --- | --- | --- |
| [Domain Search](actions/domain-search.md) | GET | Finds company email patterns in ZeroBounce by domain. |

### Domain Search Files

| Action | Method | Description |
| --- | --- | --- |
| [Bulk Domain Search File Status](actions/bulk-domain-search-file-status.md) | GET | Retrieves a bulk domain search file status from ZeroBounce. |
| [Bulk Domain Search Get File](actions/bulk-domain-search-get-file.md) | GET | Retrieves a bulk domain search file from ZeroBounce. |

### Email Finder Files

| Action | Method | Description |
| --- | --- | --- |
| [Bulk Find Email File Status](actions/bulk-find-email-file-status.md) | GET | Retrieves a bulk email finder file status from ZeroBounce. |
| [Bulk Find Email Get File](actions/bulk-find-email-get-file.md) | GET | Retrieves a bulk email finder file from ZeroBounce. |

### Evaluated Lists

| Action | Method | Description |
| --- | --- | --- |
| [Get Evaluated List Status](actions/get-evaluated-list-status.md) | GET | Retrieves a list evaluation status from ZeroBounce. |

### Scores

| Action | Method | Description |
| --- | --- | --- |
| [Score Email](actions/score-email.md) | GET | Retrieves an email score from ZeroBounce. |

### Scoring Files

| Action | Method | Description |
| --- | --- | --- |
| [Get Scoring File](actions/get-scoring-file.md) | GET | Retrieves a bulk scoring file from ZeroBounce. |
| [Get Scoring File Status](actions/get-scoring-file-status.md) | GET | Retrieves a bulk scoring file status from ZeroBounce. |

### Validation

| Action | Method | Description |
| --- | --- | --- |
| [Validate Email](actions/validate-email.md) | GET | Retrieves email validation details from ZeroBounce. |
| [Validate Email Batch](actions/validate-email-batch.md) | GET | Finds email validation results in ZeroBounce by batch request. |

### Validation Files

| Action | Method | Description |
| --- | --- | --- |
| [Get Validation File](actions/get-validation-file.md) | GET | Retrieves a bulk validation file from ZeroBounce. |
| [Get Validation File Status](actions/get-validation-file-status.md) | GET | Retrieves a bulk validation file status from ZeroBounce. |

### Validation Filters

| Action | Method | Description |
| --- | --- | --- |
| [List Validation Filters](actions/list-validation-filters.md) | GET | Retrieves custom validation filters from ZeroBounce. |

