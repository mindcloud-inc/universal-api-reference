# Enrich.so: Native API Reference

A consolidated summary of Enrich.so's API configuration and 30 documented operations, with links to official documentation.

- **Official docs:** https://doc.enrich.so/
- **API base URL:** `https://dev.enrich.so/api/v3`

## Authentication

### API Key

Authenticate Enrich API requests with a provider API key in the x-api-key header.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
x-api-key: <apiKey>
```

[Official authentication documentation](https://doc.enrich.so/authentication-1951026m0.md)

## API conventions

Responses from this API use JSON. Response data is read from `data`.

## Pagination

Use `limit` in the query string to set the page size (default 100; accepted range 1–500). Use `page` in the query string to choose the page; numbering starts at 1.

## Retry behavior

Retry responses with status codes `429,500,502,503,504`. Wait 1 ms before the first retry. Stop after 3 attempts. Multiply the delay by 2 after each failed attempt.

## Endpoints (30 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Cascading ICP People Search](actions/cascading-icp-people-search.md) | `POST /people-search/waterfall-icp-search` | [docs](https://doc.enrich.so/cascading-icp-people-search-28537859e0.md) |
| [Check Batch Finder Progress](actions/check-batch-finder-progress.md) | `GET /email-finder/batch/{batchId}` | [docs](https://doc.enrich.so/check-batch-finder-progress-27483197e0.md) |
| [Check Batch Validation Progress](actions/check-batch-validation-progress.md) | `GET /email-validation/batch/{batchId}` | [docs](https://doc.enrich.so/check-batch-validation-progress-27483193e0.md) |
| [Check Bulk Lookup Progress](actions/check-bulk-lookup-progress.md) | `GET /reverse-lookup/bulk-lookup/{batchId}` | [docs](https://doc.enrich.so/check-bulk-lookup-progress-27483205e0.md) |
| [Check Bulk Phone Lookup Progress](actions/check-bulk-phone-lookup-progress.md) | `GET /reverse-lookup/phones/bulk/{jobId}` | [docs](https://doc.enrich.so/check-bulk-phone-lookup-progress-27483201e0.md) |
| [Check Daily Scraping Limit](actions/check-daily-scraping-limit.md) | `GET /company-follower/limit` | [docs](https://doc.enrich.so/check-daily-scraping-limit-27814759e0.md) |
| [Count Matching Leads](actions/count-matching-leads.md) | `POST /lead-finder/count` | [docs](https://doc.enrich.so/count-matching-leads-28165854e0.md) |
| [Find Emails in Batch](actions/find-emails-in-batch.md) | `POST /email-finder/batch` | [docs](https://doc.enrich.so/find-emails-in-batch-27483196e0.md) |
| [Find Employees At A Company](actions/find-employees-at-company.md) | `POST /people-search/employee-finder` | [docs](https://doc.enrich.so/find-employees-at-a-company-28537860e0.md) |
| [Find Phone Numbers](actions/find-phone-numbers.md) | `GET /reverse-lookup/phones` | [docs](https://doc.enrich.so/find-phone-numbers-27483199e0.md) |
| [Find Phone Numbers in Batch](actions/find-phone-numbers-in-batch.md) | `POST /reverse-lookup/phones/bulk` | [docs](https://doc.enrich.so/find-phone-numbers-in-batch-27483200e0.md) |
| [Find a Professional Email](actions/find-professional-email.md) | `POST /email-finder` | [docs](https://doc.enrich.so/find-a-professional-email-27483195e0.md) |
| [Get Batch Finder Results](actions/get-batch-finder-results.md) | `GET /email-finder/batch/{batchId}/results` | [docs](https://doc.enrich.so/get-batch-finder-results-27483198e0.md) |
| [Get Batch Validation Results](actions/get-batch-validation-results.md) | `GET /email-validation/batch/{batchId}/results` | [docs](https://doc.enrich.so/get-batch-validation-results-27483194e0.md) |
| [Get Bulk Lookup Results](actions/get-bulk-lookup-results.md) | `GET /reverse-lookup/bulk-lookup/{batchId}/results` | [docs](https://doc.enrich.so/get-bulk-lookup-results-27483206e0.md) |
| [Get Bulk Phone Lookup Results](actions/get-bulk-phone-lookup-results.md) | `GET /reverse-lookup/phones/bulk/{jobId}/results` | [docs](https://doc.enrich.so/get-bulk-phone-lookup-results-27483202e0.md) |
| [Get Credit Balance](actions/get-credit-balance.md) | `GET /wallets/balance` | [docs](https://doc.enrich.so/get-your-credit-balance-27483207e0.md) |
| [Get Filter Options](actions/get-filter-options.md) | `GET /lead-finder/filter-options` | [docs](https://doc.enrich.so/get-filter-options-28165862e0.md) |
| [Get Transaction History](actions/get-transaction-history.md) | `GET /wallets/transactions` | [docs](https://doc.enrich.so/get-transaction-history-27483208e0.md) |
| [List Pending Invitations](actions/list-pending-invitations.md) | `GET /teams/{teamId}/invitations` | [docs](https://doc.enrich.so/list-pending-invitations-27483211e0.md) |
| [List Reveal Or Enrich Jobs](actions/list-reveal-or-enrich-jobs.md) | `GET /lead-finder/reveal-jobs` | [docs](https://doc.enrich.so/list-revealenrich-jobs-29163792e0.md) |
| [List Saved Searches](actions/list-saved-searches.md) | `GET /lead-finder/saved` | [docs](https://doc.enrich.so/list-saved-searches-28165859e0.md) |
| [List Team Members](actions/list-team-members.md) | `GET /teams/{teamId}/members` | [docs](https://doc.enrich.so/list-team-members-27483209e0.md) |
| [Look Up a Professional Profile by Email](actions/look-up-professional-profile-by-email.md) | `POST /reverse-lookup/lookup` | [docs](https://doc.enrich.so/look-up-a-professional-profile-by-email-27483203e0.md) |
| [Look Up Professional Profiles in Batch](actions/look-up-professional-profiles-in-batch.md) | `POST /reverse-lookup/bulk-lookup` | [docs](https://doc.enrich.so/look-up-professional-profiles-in-batch-27483204e0.md) |
| [Poll Reveal Or Enrich Job](actions/poll-reveal-or-enrich-job.md) | `GET /lead-finder/reveal-jobs/{jobId}` | [docs](https://doc.enrich.so/poll-revealenrich-job-29163791e0.md) |
| [Search Leads](actions/search-leads.md) | `POST /lead-finder/search` | [docs](https://doc.enrich.so/search-leads-28165853e0.md) |
| [Suggest Company Names](actions/suggest-company-names.md) | `GET /lead-finder/suggest` | [docs](https://doc.enrich.so/suggest-company-names-28165863e0.md) |
| [Validate Emails in Batch](actions/validate-emails-in-batch.md) | `POST /email-validation/batch` | [docs](https://doc.enrich.so/validate-emails-in-batch-27483192e0.md) |
| [Validate a Single Email](actions/validate-single-email.md) | `POST /email-validation` | [docs](https://doc.enrich.so/validate-a-single-email-27483191e0.md) |
