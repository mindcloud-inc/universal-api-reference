# <img src="https://mindcloud.imgix.net/apps/icons/jobber_1773083150934.png" alt="Jobber logo" width="28" height="28"> Jobber: Universal API

Manage clients, jobs, quotes, invoices, and field service work

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/jobber/latest
- **Category:** Support / Field Service
- **Actions:** 20
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.getjobber.com/
- **Vendor API docs:** https://developer.getjobber.com/docs/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Current User](actions/get-current-user.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/jobber/latest/actions/get-current-user?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (20)

### Appointments

| Action | Method | Description |
| --- | --- | --- |
| [Get Visit](actions/get-visit.md) | GET |  |

### Client

| Action | Method | Description |
| --- | --- | --- |
| [Create Client](actions/create-client.md) | POST |  |
| [Edit Client](actions/edit-client.md) | PUT |  |

### Current User

| Action | Method | Description |
| --- | --- | --- |
| [Get Current User](actions/get-current-user.md) | GET |  |

### Customers

| Action | Method | Description |
| --- | --- | --- |
| [List Clients](actions/list-clients.md) | GET |  |

### Invoices

| Action | Method | Description |
| --- | --- | --- |
| [List Invoices](actions/list-invoices.md) | GET |  |

### Job

| Action | Method | Description |
| --- | --- | --- |
| [Close Job](actions/close-job.md) | PUT |  |
| [Create Job](actions/create-job.md) | POST |  |
| [Create Job Lines](actions/create-job-lines.md) | POST |  |
| [Get Job](actions/get-job.md) | GET |  |
| [Get Job Lines](actions/get-job-lines.md) | GET |  |

### Jobs

| Action | Method | Description |
| --- | --- | --- |
| [List Jobs](actions/list-jobs.md) | GET |  |

### Other

| Action | Method | Description |
| --- | --- | --- |
| [Execute GraphQL](actions/execute-graphql.md) | GET |  |

### Payment

| Action | Method | Description |
| --- | --- | --- |
| [List Payments](actions/list-payments.md) | GET |  |

### Product Or Service

| Action | Method | Description |
| --- | --- | --- |
| [Create Item](actions/create-item.md) | POST |  |
| [List Items](actions/list-items.md) | GET |  |
| [Update Item](actions/update-item.md) | PUT |  |

### Property

| Action | Method | Description |
| --- | --- | --- |
| [Create Property on Client](actions/create-property-on-client.md) | POST |  |
| [Get Client Properties](actions/get-client-properties.md) | GET |  |

### Quote

| Action | Method | Description |
| --- | --- | --- |
| [List Quotes](actions/list-quotes.md) | GET |  |

