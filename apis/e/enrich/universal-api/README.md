# <img src="https://images.mindcloud.co/apps/icons/images-15_1774634557037.png" alt="Enrich.so logo" width="28" height="28"> Enrich.so: Universal API

Enrich API integration for enriching and validating contact, lead, company, phone, wallet, and team data through the official v3 REST API.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/enrich/latest
- **Category:** Sales & CRM / CRM
- **Actions:** 30
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.enrich.so/
- **Vendor API docs:** https://doc.enrich.so/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Credit Balance](actions/get-credit-balance.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/enrich/latest/actions/get-credit-balance?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (30)

### API Keys

| Action | Method | Description |
| --- | --- | --- |
| [Check Daily Scraping Limit](actions/check-daily-scraping-limit.md) | GET | Retrieves daily scraping limits from Enrich.so. |

### Companies

| Action | Method | Description |
| --- | --- | --- |
| [Suggest Company Names](actions/suggest-company-names.md) | GET | Finds company name suggestions in Enrich.so. |

### Contacts

| Action | Method | Description |
| --- | --- | --- |
| [Find a Professional Email](actions/find-professional-email.md) | GET | Finds a professional email in Enrich.so. |
| [Get Batch Finder Results](actions/get-batch-finder-results.md) | GET | Retrieves batch email finder results from Enrich.so. |
| [Get Batch Validation Results](actions/get-batch-validation-results.md) | GET | Retrieves batch email validation results from Enrich.so. |
| [Get Bulk Lookup Results](actions/get-bulk-lookup-results.md) | GET | Retrieves bulk profile lookup results from Enrich.so. |
| [Validate a Single Email](actions/validate-single-email.md) | GET | Validates an email address in Enrich.so. |

### Credit Usage

| Action | Method | Description |
| --- | --- | --- |
| [Get Credit Balance](actions/get-credit-balance.md) | GET | Retrieves credit balance from Enrich.so. |

### Employees

| Action | Method | Description |
| --- | --- | --- |
| [Find Employees At A Company](actions/find-employees-at-company.md) | GET | Finds company employees in Enrich.so by LinkedIn URL. |

### Invitations

| Action | Method | Description |
| --- | --- | --- |
| [List Pending Invitations](actions/list-pending-invitations.md) | GET | Retrieves pending team invitations from Enrich.so. |

### Jobs

| Action | Method | Description |
| --- | --- | --- |
| [Check Batch Finder Progress](actions/check-batch-finder-progress.md) | GET | Retrieves batch email finder progress from Enrich.so. |
| [Check Batch Validation Progress](actions/check-batch-validation-progress.md) | GET | Retrieves batch email validation progress from Enrich.so. |
| [Check Bulk Lookup Progress](actions/check-bulk-lookup-progress.md) | GET | Retrieves bulk profile lookup progress from Enrich.so. |
| [Check Bulk Phone Lookup Progress](actions/check-bulk-phone-lookup-progress.md) | GET | Retrieves bulk phone lookup progress from Enrich.so. |
| [Find Emails in Batch](actions/find-emails-in-batch.md) | POST | Creates a batch email finder job in Enrich.so. |
| [Find Phone Numbers in Batch](actions/find-phone-numbers-in-batch.md) | POST | Creates a bulk phone lookup job in Enrich.so. |
| [List Reveal Or Enrich Jobs](actions/list-reveal-or-enrich-jobs.md) | GET | Retrieves reveal or enrich jobs from Enrich.so. |
| [Look Up Professional Profiles in Batch](actions/look-up-professional-profiles-in-batch.md) | POST | Creates a bulk profile lookup job in Enrich.so. |
| [Poll Reveal Or Enrich Job](actions/poll-reveal-or-enrich-job.md) | GET | Retrieves reveal or enrich job status from Enrich.so. |
| [Validate Emails in Batch](actions/validate-emails-in-batch.md) | POST | Creates a batch email validation job in Enrich.so. |

### Leads

| Action | Method | Description |
| --- | --- | --- |
| [Cascading ICP People Search](actions/cascading-icp-people-search.md) | GET | Finds people in Enrich.so by cascading ICP filters. |
| [Count Matching Leads](actions/count-matching-leads.md) | GET | Retrieves lead counts from Enrich.so by search filters. |
| [Search Leads](actions/search-leads.md) | GET | Finds leads in Enrich.so by search filters. |

### Phone Lookup

| Action | Method | Description |
| --- | --- | --- |
| [Find Phone Numbers](actions/find-phone-numbers.md) | GET | Finds phone numbers in Enrich.so by email or profile URL. |

### Phone Numbers

| Action | Method | Description |
| --- | --- | --- |
| [Get Bulk Phone Lookup Results](actions/get-bulk-phone-lookup-results.md) | GET | Retrieves bulk phone lookup results from Enrich.so. |

### Queries

| Action | Method | Description |
| --- | --- | --- |
| [List Saved Searches](actions/list-saved-searches.md) | GET | Retrieves saved searches from Enrich.so. |

### Reverse Email Append

| Action | Method | Description |
| --- | --- | --- |
| [Look Up a Professional Profile by Email](actions/look-up-professional-profile-by-email.md) | GET | Retrieves a professional profile by email from Enrich.so. |

### Transactions

| Action | Method | Description |
| --- | --- | --- |
| [Get Transaction History](actions/get-transaction-history.md) | GET | Retrieves credit transaction history from Enrich.so. |

### Unknown Objects

| Action | Method | Description |
| --- | --- | --- |
| [Get Filter Options](actions/get-filter-options.md) | GET | Retrieves lead filter options from Enrich.so. |

### Users

| Action | Method | Description |
| --- | --- | --- |
| [List Team Members](actions/list-team-members.md) | GET | Retrieves team members from Enrich.so. |

