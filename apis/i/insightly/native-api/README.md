# Insightly: Native API Reference

A consolidated summary of Insightly's API configuration and 30 documented operations, with links to official documentation.

- **Official docs:** https://api.insightly.com/v3.1/Help
- **OpenAPI specification:** https://api.na1.insightly.com/v3.1/swagger/docs/v3.1
- **API base URL:** `https://api.na1.insightly.com/v3.1/`

## Authentication

### Basic (API Key)

Enter your Insightly API key as the username, leave the password blank, and provide the pod-specific API base URL from Insightly User Settings > API.

### Credentials

- **Username:** `username` · required
- **Password:** `password` · required
- **API Base URL:** `apiBaseUrl` · required · Paste the full Insightly API URL shown under your API key in User Settings > API, for example https://api.na1.insightly.com/v3.1/.

Join the username and password with a colon, Base64-encode the result, and send it with the `Basic` authorization scheme:

```js
const credentials = Buffer.from(`${username}:${password}`).toString('base64');

const response = await fetch(url, {
  headers: {
    Authorization: `Basic ${credentials}`
  }
});
```

[Official authentication documentation](https://api.na1.insightly.com/v3.1/#!/Overview/Introduction)

## Pagination

Use `top` in the query string to set the page size (default 100; maximum 500). Use `skip` in the query string as the record offset.

## Endpoints (30 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Contact](actions/create-contact.md) | `POST {{credentials.apiBaseUrl}}Contacts` | [docs](https://api.insightly.com/v3.1/Help#!/Contacts/AddEntity) |
| [Create Lead](actions/create-lead.md) | `POST {{credentials.apiBaseUrl}}Leads` | [docs](https://api.insightly.com/v3.1/Help#!/Leads/AddEntity) |
| [Create Opportunity](actions/create-opportunity.md) | `POST {{credentials.apiBaseUrl}}Opportunities` | [docs](https://api.insightly.com/v3.1/Help#!/Opportunities/AddEntity) |
| [Create Organisation](actions/create-organisation.md) | `POST {{credentials.apiBaseUrl}}Organisations` | [docs](https://api.insightly.com/v3.1/Help#!/Organisations/AddEntity) |
| [Create Project](actions/create-project.md) | `POST {{credentials.apiBaseUrl}}Projects` | [docs](https://api.insightly.com/v3.1/Help#!/Projects/AddEntity) |
| [Create Task](actions/create-task.md) | `POST {{credentials.apiBaseUrl}}Tasks` | [docs](https://api.insightly.com/v3.1/Help#!/Tasks/AddEntity) |
| [Get Contact](actions/get-contact.md) | `GET {{credentials.apiBaseUrl}}Contacts/:contactId` | [docs](https://api.insightly.com/v3.1/Help#!/Contacts/GetEntity) |
| [Get Lead](actions/get-lead.md) | `GET {{credentials.apiBaseUrl}}Leads/:leadId` | [docs](https://api.insightly.com/v3.1/Help#!/Leads/GetEntity) |
| [Get Opportunity](actions/get-opportunity.md) | `GET {{credentials.apiBaseUrl}}Opportunities/:opportunityId` | [docs](https://api.insightly.com/v3.1/Help#!/Opportunities/GetEntity) |
| [Get Organisation](actions/get-organisation.md) | `GET {{credentials.apiBaseUrl}}Organisations/:organisationId` | [docs](https://api.insightly.com/v3.1/Help#!/Organisations/GetEntity) |
| [Get Project](actions/get-project.md) | `GET {{credentials.apiBaseUrl}}Projects/:projectId` | [docs](https://api.insightly.com/v3.1/Help#!/Projects/GetEntity) |
| [Get Task](actions/get-task.md) | `GET {{credentials.apiBaseUrl}}Tasks/:taskId` | [docs](https://api.insightly.com/v3.1/Help#!/Tasks/GetEntity) |
| [List Contacts](actions/list-contacts.md) | `GET {{credentials.apiBaseUrl}}Contacts` | [docs](https://api.insightly.com/v3.1/Help#!/Contacts/GetEntities) |
| [List Leads](actions/list-leads.md) | `GET {{credentials.apiBaseUrl}}Leads` | [docs](https://api.insightly.com/v3.1/Help#!/Leads/GetEntities) |
| [List Opportunities](actions/list-opportunities.md) | `GET {{credentials.apiBaseUrl}}Opportunities` | [docs](https://api.insightly.com/v3.1/Help#!/Opportunities/GetEntities) |
| [List Organisations](actions/list-organisations.md) | `GET {{credentials.apiBaseUrl}}Organisations` | [docs](https://api.insightly.com/v3.1/Help#!/Organisations/GetEntities) |
| [List Projects](actions/list-projects.md) | `GET {{credentials.apiBaseUrl}}Projects` | [docs](https://api.insightly.com/v3.1/Help#!/Projects/GetEntities) |
| [List Tasks](actions/list-tasks.md) | `GET {{credentials.apiBaseUrl}}Tasks` | [docs](https://api.insightly.com/v3.1/Help#!/Tasks/GetEntities) |
| [Search Contacts](actions/search-contacts.md) | `GET {{credentials.apiBaseUrl}}Contacts/Search` | [docs](https://api.insightly.com/v3.1/Help#!/Contacts/GetEntitiesBySearch) |
| [Search Leads](actions/search-leads.md) | `GET {{credentials.apiBaseUrl}}Leads/Search` | [docs](https://api.insightly.com/v3.1/Help#!/Leads/GetEntitiesBySearch) |
| [Search Opportunities](actions/search-opportunities.md) | `GET {{credentials.apiBaseUrl}}Opportunities/Search` | [docs](https://api.insightly.com/v3.1/Help#!/Opportunities/GetEntitiesBySearch) |
| [Search Organisations](actions/search-organisations.md) | `GET {{credentials.apiBaseUrl}}Organisations/Search` | [docs](https://api.insightly.com/v3.1/Help#!/Organisations/GetEntitiesBySearch) |
| [Search Projects](actions/search-projects.md) | `GET {{credentials.apiBaseUrl}}Projects/Search` | [docs](https://api.insightly.com/v3.1/Help#!/Projects/GetEntitiesBySearch) |
| [Search Tasks](actions/search-tasks.md) | `GET {{credentials.apiBaseUrl}}Tasks/Search` | [docs](https://api.insightly.com/v3.1/Help#!/Tasks/GetEntitiesBySearch) |
| [Update Contact](actions/update-contact.md) | `PUT {{credentials.apiBaseUrl}}Contacts` | [docs](https://api.insightly.com/v3.1/Help#!/Contacts/UpdateEntity) |
| [Update Lead](actions/update-lead.md) | `PUT {{credentials.apiBaseUrl}}Leads` | [docs](https://api.insightly.com/v3.1/Help#!/Leads/UpdateEntity) |
| [Update Opportunity](actions/update-opportunity.md) | `PUT {{credentials.apiBaseUrl}}Opportunities` | [docs](https://api.insightly.com/v3.1/Help#!/Opportunities/UpdateEntity) |
| [Update Organisation](actions/update-organisation.md) | `PUT {{credentials.apiBaseUrl}}Organisations` | [docs](https://api.insightly.com/v3.1/Help#!/Organisations/UpdateEntity) |
| [Update Project](actions/update-project.md) | `PUT {{credentials.apiBaseUrl}}Projects` | [docs](https://api.insightly.com/v3.1/Help#!/Projects/UpdateEntity) |
| [Update Task](actions/update-task.md) | `PUT {{credentials.apiBaseUrl}}Tasks` | [docs](https://api.insightly.com/v3.1/Help#!/Tasks/UpdateEntity) |
