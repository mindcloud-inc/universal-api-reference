# <img src="https://images.mindcloud.co/apps/icons/streamtime_1773328903227.png" alt="Streamtime logo" width="28" height="28"> Streamtime: Universal API

Plan jobs, track time, invoice clients, and report profitability

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/streamtime/latest
- **Category:** Productivity / Project Management
- **Actions:** 24
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.streamtime.net
- **Vendor API docs:** https://api.streamtime.net/v2/swagger

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Organisation](actions/get-organisation.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/streamtime/latest/actions/get-organisation?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (24)

### Company

| Action | Method | Description |
| --- | --- | --- |
| [Create Company](actions/create-company.md) | POST |  |
| [Get Company](actions/get-company.md) | GET |  |

### Contact

| Action | Method | Description |
| --- | --- | --- |
| [Create Company Contact](actions/create-company-contact.md) | POST |  |
| [List Company Contacts](actions/list-company-contacts.md) | GET |  |

### Invoice

| Action | Method | Description |
| --- | --- | --- |
| [Get Invoice](actions/get-invoice.md) | GET |  |

### Invoice Line Item

| Action | Method | Description |
| --- | --- | --- |
| [List Invoice Line Items](actions/list-invoice-line-items.md) | GET |  |

### Job

| Action | Method | Description |
| --- | --- | --- |
| [Create Job](actions/create-job.md) | POST |  |
| [Get Job](actions/get-job.md) | GET |  |
| [Update Job](actions/update-job.md) | PUT |  |

### Job Item

| Action | Method | Description |
| --- | --- | --- |
| [Create Job Item](actions/create-job-item.md) | POST |  |
| [List Job Items](actions/list-job-items.md) | GET |  |

### Job Phase

| Action | Method | Description |
| --- | --- | --- |
| [Create Job Phase](actions/create-job-phase.md) | POST |  |
| [List Job Phases](actions/list-job-phases.md) | GET |  |

### Job Status

| Action | Method | Description |
| --- | --- | --- |
| [Update Job Status](actions/update-job-status.md) | PUT |  |

### Logged Time

| Action | Method | Description |
| --- | --- | --- |
| [Create Logged Time Entry](actions/create-logged-time-entry.md) | POST |  |
| [Create Multiple Logged Time Entries](actions/create-multiple-logged-time-entries.md) | POST |  |
| [Get Logged Time Entry](actions/get-logged-time-entry.md) | GET |  |
| [Update Logged Time Entry](actions/update-logged-time-entry.md) | PUT |  |

### Organisation

| Action | Method | Description |
| --- | --- | --- |
| [Get Organisation](actions/get-organisation.md) | GET |  |

### Quote

| Action | Method | Description |
| --- | --- | --- |
| [Get Quote](actions/get-quote.md) | GET |  |

### Quote Line Item

| Action | Method | Description |
| --- | --- | --- |
| [List Quote Line Items](actions/list-quote-line-items.md) | GET |  |

### Search Result

| Action | Method | Description |
| --- | --- | --- |
| [Search Records](actions/search-records.md) | GET |  |

### User

| Action | Method | Description |
| --- | --- | --- |
| [Get User](actions/get-user.md) | GET |  |
| [List Users](actions/list-users.md) | GET |  |

