# Kylas CRM: Native API Reference

A consolidated summary of Kylas CRM's API configuration and 32 documented operations, with links to official documentation.

- **Official docs:** https://www.postman.com/kylasqa/kylas-apis/documentation/awdync1/kylas-apis-public
- **API base URL:** `https://api.kylas.io/v1`

## Authentication

### Kylas API Header

Authenticate Kylas requests with the Api-Key header.

### Credentials

- **API Key:** `apiKey` · optional · Your Kylas tenant API key.

Send these headers with each API request:

```http
Api-Key: <apiKey>
```

[Official authentication documentation](https://support.kylas.io/portal/en/kb/articles/how-to-use-api-key-in-to-access-kylas-apis)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Endpoints (32 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Add Currencies](actions/add-currencies.md) | `POST /forex/currencies` | [docs](https://www.postman.com/kylasqa/kylas-apis/documentation/awdync1/kylas-apis-public) |
| [Check Lead Duplicates](actions/check-lead-duplicates.md) | `GET /leads/{leadId}/has-duplicates` | [docs](https://www.postman.com/kylasqa/kylas-apis/documentation/awdync1/kylas-apis-public) |
| [Create Contact](actions/create-contact.md) | `POST /contacts` | [docs](https://www.postman.com/kylasqa/kylas-apis/documentation/awdync1/kylas-apis-public) |
| [Create Lead](actions/create-lead.md) | `POST /leads` | [docs](https://www.postman.com/kylasqa/kylas-apis/documentation/awdync1/kylas-apis-public) |
| [Delete Contact](actions/delete-contact.md) | `DELETE /contacts/{contactId}` | [docs](https://www.postman.com/kylasqa/kylas-apis/documentation/awdync1/kylas-apis-public) |
| [Delete Lead](actions/delete-lead.md) | `DELETE /leads/{leadId}` | [docs](https://www.postman.com/kylasqa/kylas-apis/documentation/awdync1/kylas-apis-public) |
| [Get Contact](actions/get-contact.md) | `GET /contacts/{contactId}` | [docs](https://www.postman.com/kylasqa/kylas-apis/documentation/awdync1/kylas-apis-public) |
| [Get Contact Layout](actions/get-contact-layout.md) | `GET /ui/layouts/EDIT/CONTACT` | [docs](https://www.postman.com/kylasqa/kylas-apis/documentation/awdync1/kylas-apis-public) |
| [Get Lead](actions/get-lead.md) | `GET /leads/{leadId}` | [docs](https://www.postman.com/kylasqa/kylas-apis/documentation/awdync1/kylas-apis-public) |
| [Get Lead Layout](actions/get-lead-layout.md) | `GET /ui/layouts/CREATE/LEAD` | [docs](https://www.postman.com/kylasqa/kylas-apis/documentation/awdync1/kylas-apis-public) |
| [Get Task Create Layout](actions/get-task-create-layout.md) | `GET /ui/layouts/CREATE/TASK` | [docs](https://www.postman.com/kylasqa/kylas-apis/documentation/awdync1/kylas-apis-public) |
| [Get User](actions/get-user.md) | `GET /users/{userId}` | [docs](https://www.postman.com/kylasqa/kylas-apis/documentation/awdync1/kylas-apis-public) |
| [List Active Currencies](actions/list-active-currencies.md) | `GET /forex/currencies` | [docs](https://www.postman.com/kylasqa/kylas-apis/documentation/awdync1/kylas-apis-public) |
| [List Contacts](actions/list-contacts.md) | `GET /contacts` | [docs](https://www.postman.com/kylasqa/kylas-apis/documentation/awdync1/kylas-apis-public) |
| [List Fields](actions/list-fields.md) | `GET /fields` | [docs](https://www.postman.com/kylasqa/kylas-apis/documentation/awdync1/kylas-apis-public) |
| [List Tasks](actions/list-tasks.md) | `GET /tasks` | [docs](https://www.postman.com/kylasqa/kylas-apis/documentation/awdync1/kylas-apis-public) |
| [List Teams](actions/list-teams.md) | `GET /teams` | [docs](https://www.postman.com/kylasqa/kylas-apis/documentation/awdync1/kylas-apis-public) |
| [List Users](actions/list-users.md) | `GET /users` | [docs](https://www.postman.com/kylasqa/kylas-apis/documentation/awdync1/kylas-apis-public) |
| [Lookup Contacts](actions/lookup-contacts.md) | `GET /search/contact/lookup` | [docs](https://www.postman.com/kylasqa/kylas-apis/documentation/awdync1/kylas-apis-public) |
| [Lookup Deal Pipelines](actions/lookup-deal-pipelines.md) | `GET /pipelines/lookup?entityType=DEAL` | [docs](https://www.postman.com/kylasqa/kylas-apis/documentation/awdync1/kylas-apis-public) |
| [Lookup Deals](actions/lookup-deals.md) | `GET /search/deal/lookup` | [docs](https://www.postman.com/kylasqa/kylas-apis/documentation/awdync1/kylas-apis-public) |
| [Lookup Lead Pipelines](actions/lookup-lead-pipelines.md) | `GET /pipelines/lookup?entityType=LEAD` | [docs](https://www.postman.com/kylasqa/kylas-apis/documentation/awdync1/kylas-apis-public) |
| [Lookup Leads](actions/lookup-leads.md) | `GET /search/lead/lookup` | [docs](https://www.postman.com/kylasqa/kylas-apis/documentation/awdync1/kylas-apis-public) |
| [Lookup Teams](actions/lookup-teams.md) | `GET /teams/lookup` | [docs](https://www.postman.com/kylasqa/kylas-apis/documentation/awdync1/kylas-apis-public) |
| [Lookup Users](actions/lookup-users.md) | `GET /users/lookup` | [docs](https://www.postman.com/kylasqa/kylas-apis/documentation/awdync1/kylas-apis-public) |
| [Search Contacts](actions/search-contacts.md) | `POST /search/contact?page=0&size=10&sort=updatedAt,desc` | [docs](https://www.postman.com/kylasqa/kylas-apis/documentation/awdync1/kylas-apis-public) |
| [Search Deals](actions/search-deals.md) | `POST /search/deal?page=0&size=10&sort=updatedAt,desc` | [docs](https://www.postman.com/kylasqa/kylas-apis/documentation/awdync1/kylas-apis-public) |
| [Search Leads](actions/search-leads.md) | `POST /search/lead?page=0&size=10&sort=updatedAt,desc` | [docs](https://www.postman.com/kylasqa/kylas-apis/documentation/awdync1/kylas-apis-public) |
| [Search Pipelines](actions/search-pipelines.md) | `POST /pipelines/search?sort=updatedAt,desc&page=0&size=100` | [docs](https://www.postman.com/kylasqa/kylas-apis/documentation/awdync1/kylas-apis-public) |
| [Search Users](actions/search-users.md) | `POST /users/search?sort=updatedAt,desc&page=0&size=20` | [docs](https://www.postman.com/kylasqa/kylas-apis/documentation/awdync1/kylas-apis-public) |
| [Update Contact](actions/update-contact.md) | `PUT /contacts/{contactId}` | [docs](https://www.postman.com/kylasqa/kylas-apis/documentation/awdync1/kylas-apis-public) |
| [Update Lead](actions/update-lead.md) | `PUT /leads/{leadId}` | [docs](https://www.postman.com/kylasqa/kylas-apis/documentation/awdync1/kylas-apis-public) |
