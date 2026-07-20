# Salesflare: Native API Reference

A consolidated summary of Salesflare's API configuration and 25 documented operations, with links to official documentation.

- **Official docs:** https://api.salesflare.com/docs#section/Introduction/Authentication
- **OpenAPI specification:** https://api.salesflare.com/openapi.json
- **API base URL:** `https://api.salesflare.com`

## Authentication

### API Key

Authenticate with a Salesflare API key sent as a Bearer token in the Authorization header.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://howto.salesflare.com/en/articles/1017460-do-you-have-an-api)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Pagination

Use `limit` in the query string to set the page size (default 100; minimum 1). Use `offset` in the query string as the record offset; numbering starts at 0.

## Filtering

Send filters in the query string.

## Sorting

Set the sort field with `order_by` in the query string. Use `ascending` for ascending order and `desc` for descending order. Multiple sort fields can be combined.

## Endpoints (25 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Account](actions/create-account.md) | `POST accounts` | [docs](https://api.salesflare.com/docs#/Accounts/postAccounts) |
| [Create Contact](actions/create-contact.md) | `POST contacts` | [docs](https://api.salesflare.com/docs#/Contacts/postContacts) |
| [Create Opportunity](actions/create-opportunity.md) | `POST opportunities` | [docs](https://api.salesflare.com/docs#/Opportunities/postOpportunities) |
| [Create Task](actions/create-task.md) | `POST tasks` | [docs](https://api.salesflare.com/docs#/Tasks/postTasks) |
| [Delete Account](actions/delete-account.md) | `DELETE accounts/:account_id` | [docs](https://api.salesflare.com/docs#/Accounts/deleteAccountsAccount_id) |
| [Delete Contact](actions/delete-contact.md) | `DELETE contacts/:contact_id` | [docs](https://api.salesflare.com/docs#/Contacts/deleteContactsContact_id) |
| [Delete Opportunity](actions/delete-opportunity.md) | `DELETE opportunities/:id` | [docs](https://api.salesflare.com/docs#/Opportunities/deleteOpportunitiesId) |
| [Delete Task](actions/delete-task.md) | `DELETE tasks/:id` | [docs](https://api.salesflare.com/docs#/Tasks/deleteTasksId) |
| [Get Account](actions/get-account.md) | `GET accounts` | [docs](https://api.salesflare.com/docs#/Accounts/getAccountsAccount_id) |
| [Get Contact](actions/get-contact.md) | `GET contacts` | [docs](https://api.salesflare.com/docs#/Contacts/getContactsContact_id) |
| [Get Current User](actions/get-current-user.md) | `GET me` | [docs](https://api.salesflare.com/docs#/Users/getMe) |
| [Get Opportunity](actions/get-opportunity.md) | `GET opportunities` | [docs](https://api.salesflare.com/docs#/Opportunities/getOpportunitiesId) |
| [Get Stage](actions/get-stage.md) | `GET stages` | [docs](https://api.salesflare.com/docs#/Pipelines/getStagesStage_id) |
| [Get User](actions/get-user.md) | `GET users` | [docs](https://api.salesflare.com/docs#/Users/getUsersId) |
| [List Accounts](actions/list-accounts.md) | `GET accounts` | [docs](https://api.salesflare.com/docs#/Accounts/getAccounts) |
| [List Contacts](actions/list-contacts.md) | `GET contacts` | [docs](https://api.salesflare.com/docs#/Contacts/getContacts) |
| [List Opportunities](actions/list-opportunities.md) | `GET opportunities` | [docs](https://api.salesflare.com/docs#/Opportunities/getOpportunities) |
| [List Pipelines](actions/list-pipelines.md) | `GET pipelines` | [docs](https://api.salesflare.com/docs#/Pipelines/getPipelines) |
| [List Stages](actions/list-stages.md) | `GET stages` | [docs](https://api.salesflare.com/docs#/Pipelines/getStages) |
| [List Tasks](actions/list-tasks.md) | `GET tasks` | [docs](https://api.salesflare.com/docs#/Tasks/getTasks) |
| [List Users](actions/list-users.md) | `GET users` | [docs](https://api.salesflare.com/docs#/Users/getUsers) |
| [Update Account](actions/update-account.md) | `PUT accounts/:account_id` | [docs](https://api.salesflare.com/docs#/Accounts/putAccountsAccount_id) |
| [Update Contact](actions/update-contact.md) | `PUT contacts/:contact_id` | [docs](https://api.salesflare.com/docs#/Contacts/putContactsContact_id) |
| [Update Opportunity](actions/update-opportunity.md) | `PUT opportunities/:id` | [docs](https://api.salesflare.com/docs#/Opportunities/putOpportunitiesId) |
| [Update Task](actions/update-task.md) | `PUT tasks/:id` | [docs](https://api.salesflare.com/docs#/Tasks/putTasksId) |
