# <img src="https://images.mindcloud.co/apps/icons/leap_1777577045633.png" alt="Leap logo" width="28" height="28"> Leap: Universal API

Leap is a home-improvement CRM platform. This Stage 1 draft uses the provider-generated dashboard access token from Settings -> Developers and calls the official Leap REST API over Bearer authentication.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/leap/latest
- **Category:** Sales & CRM / CRM
- **Actions:** 20
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://leaptodigital.com/
- **Vendor API docs:** https://docs.api.jobprogress.com/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Company Trades](actions/list-company-trades.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/leap/latest/actions/list-company-trades?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (20)

### Category

| Action | Method | Description |
| --- | --- | --- |
| [List Categories](actions/list-categories.md) | GET | Retrieves item category records from Leap. |

### Company Trade

| Action | Method | Description |
| --- | --- | --- |
| [List Company Trades](actions/list-company-trades.md) | GET | Retrieves company trade records from Leap. |

### Country

| Action | Method | Description |
| --- | --- | --- |
| [List Countries](actions/list-countries.md) | GET | Retrieves available country records from Leap. |

### Customer

| Action | Method | Description |
| --- | --- | --- |
| [Create Customer](actions/create-customer.md) | POST | Creates a new customer in Leap. |
| [Get Customer](actions/get-customer.md) | GET | Retrieves a customer from Leap. |
| [List Customers](actions/list-customers.md) | GET | Retrieves customer records from Leap. |
| [Update Customer](actions/update-customer.md) | PUT | Updates an existing customer in Leap. |

### Division

| Action | Method | Description |
| --- | --- | --- |
| [List Divisions](actions/list-divisions.md) | GET | Retrieves company division records from Leap. |

### Job

| Action | Method | Description |
| --- | --- | --- |
| [Create Job](actions/create-job.md) | POST | Creates a new job in Leap. |
| [Get Job](actions/get-job.md) | GET | Retrieves a job from Leap. |
| [List Jobs](actions/list-jobs.md) | GET | Retrieves job records from Leap. |
| [Update Job](actions/update-job.md) | PUT | Updates an existing job in Leap. |

### Job Note

| Action | Method | Description |
| --- | --- | --- |
| [Add Job Note](actions/add-job-note.md) | POST | Creates a new note for a job in Leap. |
| [List Job Notes](actions/list-job-notes.md) | GET | Retrieves notes for a job from Leap. |
| [Update Job Note](actions/update-job-note.md) | PUT | Updates an existing job note in Leap. |

### Payment Method

| Action | Method | Description |
| --- | --- | --- |
| [List Payment Methods](actions/list-payment-methods.md) | GET | Retrieves available payment methods from Leap. |

### State

| Action | Method | Description |
| --- | --- | --- |
| [List States](actions/list-states.md) | GET | Retrieves states for a country from Leap. |

### Supplier

| Action | Method | Description |
| --- | --- | --- |
| [List Suppliers](actions/list-suppliers.md) | GET | Retrieves supplier records from Leap. |

### User

| Action | Method | Description |
| --- | --- | --- |
| [List Users](actions/list-users.md) | GET | Retrieves company user records from Leap. |

### Workflow Stage

| Action | Method | Description |
| --- | --- | --- |
| [List Workflow Stages](actions/list-workflow-stages.md) | GET | Retrieves workflow stage records from Leap. |

