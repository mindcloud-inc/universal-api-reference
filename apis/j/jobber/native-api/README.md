# Jobber: Native API Reference

A consolidated summary of Jobber's API configuration and 20 documented operations, with links to official documentation.

- **Official docs:** https://developer.getjobber.com/docs/
- **API base URL:** `https://api.getjobber.com/api`

## Authentication

### OAuth 2.0

Connect your Jobber account with OAuth 2.0

Register an OAuth application with the provider to obtain client credentials and configure its redirect URI.

1. Send the user to https://api.getjobber.com/api/oauth/authorize to approve access.
2. Exchange the returned authorization code with a POST request to https://api.getjobber.com/api/oauth/token.
3. Send the resulting access token as `Authorization: Bearer <accessToken>` on API requests.


The flow supports refresh tokens. Refresh expired access tokens with a POST request to https://api.getjobber.com/api/oauth/token.

[Official authentication documentation](https://developer.getjobber.com/docs/building_your_app/app_authorization/)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |
| `X-JOBBER-GRAPHQL-VERSION` | `2025-04-16` |

Responses from this API use JSON.

## Pagination

Use `limit` in the request parameters to set the page size (default 100; accepted range 1–5000). Use `cursor` in the request parameters as the pagination cursor.

## Filtering

Send filters in the request body.

## Endpoints (20 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Close Job](actions/close-job.md) | `POST graphql` | [docs](https://developer.getjobber.com/docs/using_jobbers_api/api_queries_and_mutations/) |
| [Create Client](actions/create-client.md) | `POST graphql` | [docs](https://developer.getjobber.com/docs/using_jobbers_api/api_queries_and_mutations/) |
| [Create Item](actions/create-item.md) | `POST graphql` | [docs](https://developer.getjobber.com/docs/using_jobbers_api/api_queries_and_mutations/) |
| [Create Job](actions/create-job.md) | `POST graphql` | [docs](https://developer.getjobber.com/docs/using_jobbers_api/api_queries_and_mutations/) |
| [Create Job Lines](actions/create-job-lines.md) | `POST graphql` | [docs](https://developer.getjobber.com/docs/using_jobbers_api/api_queries_and_mutations/) |
| [Create Property on Client](actions/create-property-on-client.md) | `POST graphql` | [docs](https://developer.getjobber.com/docs/using_jobbers_api/api_queries_and_mutations/) |
| [Edit Client](actions/edit-client.md) | `POST graphql` | [docs](https://developer.getjobber.com/docs/using_jobbers_api/api_queries_and_mutations/) |
| [Execute GraphQL](actions/execute-graphql.md) | `POST graphql` | [docs](https://developer.getjobber.com/docs/using_jobbers_api/api_queries_and_mutations/) |
| [Get Client Properties](actions/get-client-properties.md) | `POST graphql` | [docs](https://developer.getjobber.com/docs/using_jobbers_api/api_queries_and_mutations/) |
| [Get Current User](actions/get-current-user.md) | `POST graphql` | [docs](https://developer.getjobber.com/docs/building_your_app/manage_app_button/) |
| [Get Job](actions/get-job.md) | `POST graphql` | [docs](https://developer.getjobber.com/docs/using_jobbers_api/api_queries_and_mutations/) |
| [Get Job Lines](actions/get-job-lines.md) | `POST graphql` | [docs](https://developer.getjobber.com/docs/using_jobbers_api/api_queries_and_mutations/) |
| [Get Visit](actions/get-visit.md) | `POST graphql` |  |
| [List Clients](actions/list-clients.md) | `POST graphql` |  |
| [List Invoices](actions/list-invoices.md) | `POST graphql` | [docs](https://developer.getjobber.com/docs/) |
| [List Items](actions/list-items.md) | `POST graphql` | [docs](https://developer.getjobber.com/docs/) |
| [List Jobs](actions/list-jobs.md) | `POST graphql` | [docs](https://developer.getjobber.com/docs/api-reference/queries/jobs) |
| [List Payments](actions/list-payments.md) | `POST graphql` | [docs](https://developer.getjobber.com/docs/) |
| [List Quotes](actions/list-quotes.md) | `POST graphql` | [docs](https://developer.getjobber.com/docs/) |
| [Update Item](actions/update-item.md) | `POST graphql` | [docs](https://developer.getjobber.com/docs/using_jobbers_api/api_queries_and_mutations/) |
