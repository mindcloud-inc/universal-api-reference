# Gorgias: Native API Reference

A consolidated summary of Gorgias's API configuration and 32 documented operations, with links to official documentation.

- **Official docs:** https://developers.gorgias.com/
- **API base URL:** `https://{subdomain}.gorgias.com/api`

## Authentication

### OAuth 2.0

Authorize MindCloud against your Gorgias tenant using OAuth 2.0.

### Credentials

- **Subdomain:** `subdomain` · required · Enter the Gorgias account subdomain from your helpdesk URL. For https://mindcloud.gorgias.com, the subdomain is mindcloud.

Register an OAuth application with the provider to obtain client credentials and configure its redirect URI.

1. Send the user to https://{{credentials.subdomain}}.gorgias.com/oauth/authorize to approve access.
2. Exchange the returned authorization code with a POST request to https://{{credentials.subdomain}}.gorgias.com/oauth/token.
3. Send the resulting access token as `Authorization: Bearer <accessToken>` on API requests.

Requested scopes: `openid email profile offline write:all`.

The flow supports refresh tokens. Refresh expired access tokens with a POST request to https://{{credentials.subdomain}}.gorgias.com/oauth/token.

[Official authentication documentation](https://developers.gorgias.com/v1.1/docs/oauth2-bearer-token)

## API conventions

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |

Responses from this API use JSON.

## Pagination

Use `limit` in the query string to set the page size (default 50). Use `cursor` in the query string as the pagination cursor.

## Endpoints (32 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [List Custom Fields](actions/list-custom-fields.md) | `GET /custom-fields` | [docs](https://developers.gorgias.com/reference/list-custom-fields) |
| [List Customers](actions/list-customers.md) | `GET /customers` | [docs](https://developers.gorgias.com/reference/list-customers) |
| [List Events](actions/list-events.md) | `GET /events` | [docs](https://developers.gorgias.com/reference/list-events) |
| [List Integrations](actions/list-integrations.md) | `GET /integrations` | [docs](https://developers.gorgias.com/reference/list-integrations) |
| [List Jobs](actions/list-jobs.md) | `GET /jobs` | [docs](https://developers.gorgias.com/reference/list-jobs) |
| [List Macros](actions/list-macros.md) | `GET /macros` | [docs](https://developers.gorgias.com/reference/list-macros) |
| [List Messages](actions/list-messages.md) | `GET /messages` | [docs](https://developers.gorgias.com/reference/list-messages) |
| [List Rules](actions/list-rules.md) | `GET /rules` | [docs](https://developers.gorgias.com/reference/list-rules) |
| [List Settings](actions/list-settings.md) | `GET /settings` | [docs](https://developers.gorgias.com/reference/list-account-settings) |
| [List Surveys](actions/list-surveys.md) | `GET /surveys` | [docs](https://developers.gorgias.com/reference/list-satisfaction-surveys) |
| [List Tags](actions/list-tags.md) | `GET /tags` | [docs](https://developers.gorgias.com/reference/list-tags) |
| [List Teams](actions/list-teams.md) | `GET /teams` | [docs](https://developers.gorgias.com/reference/list-teams) |
| [List Tickets](actions/list-tickets.md) | `GET /tickets` | [docs](https://developers.gorgias.com/reference/list-tickets) |
| [List Users](actions/list-users.md) | `GET /users` | [docs](https://developers.gorgias.com/reference/list-users) |
| [List Views](actions/list-views.md) | `GET /views` | [docs](https://developers.gorgias.com/reference/list-views) |
| [List Widgets](actions/list-widgets.md) | `GET /widgets` | [docs](https://developers.gorgias.com/reference/list-widgets) |
| [Retrieve Account](actions/retrieve-account.md) | `GET /account` | [docs](https://developers.gorgias.com/reference/get-account) |
| [Retrieve Custom Field](actions/retrieve-custom-field.md) | `GET /custom-fields/:id` | [docs](https://developers.gorgias.com/reference/get-custom-field) |
| [Retrieve Customer](actions/retrieve-customer.md) | `GET /customers/:id` | [docs](https://developers.gorgias.com/reference/get-customer) |
| [Retrieve Event](actions/retrieve-event.md) | `GET /events/:id` | [docs](https://developers.gorgias.com/reference/get-event) |
| [Retrieve Integration](actions/retrieve-integration.md) | `GET /integrations/:id` | [docs](https://developers.gorgias.com/reference/get-integration) |
| [Retrieve Job](actions/retrieve-job.md) | `GET /jobs/:id` | [docs](https://developers.gorgias.com/reference/get-job) |
| [Retrieve Macro](actions/retrieve-macro.md) | `GET /macros/:id` | [docs](https://developers.gorgias.com/reference/get-macro) |
| [Retrieve Rule](actions/retrieve-rule.md) | `GET /rules/:id` | [docs](https://developers.gorgias.com/reference/get-rule) |
| [Retrieve Survey](actions/retrieve-survey.md) | `GET /surveys/:id` | [docs](https://developers.gorgias.com/reference/get-satisfaction-survey) |
| [Retrieve Tag](actions/retrieve-tag.md) | `GET /tags/:id` | [docs](https://developers.gorgias.com/reference/get-tag) |
| [Retrieve Team](actions/retrieve-team.md) | `GET /teams/:id` | [docs](https://developers.gorgias.com/reference/get-team) |
| [Retrieve Ticket](actions/retrieve-ticket.md) | `GET /tickets/:id` | [docs](https://developers.gorgias.com/reference/get-ticket) |
| [Retrieve User](actions/retrieve-user.md) | `GET /users/:id` | [docs](https://developers.gorgias.com/reference/get-user) |
| [Retrieve View](actions/retrieve-view.md) | `GET /views/:id` | [docs](https://developers.gorgias.com/reference/get-view) |
| [Retrieve Widget](actions/retrieve-widget.md) | `GET /widgets/:id` | [docs](https://developers.gorgias.com/reference/get-widget) |
| [Search Resources](actions/search-resources.md) | `GET /search` | [docs](https://developers.gorgias.com/reference/search-1) |
