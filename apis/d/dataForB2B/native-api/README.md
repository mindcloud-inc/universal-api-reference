# DataForB2B: Native API Reference

A consolidated summary of DataForB2B's API configuration and 17 documented operations, with links to official documentation.

- **Official docs:** https://docs.dataforb2b.ai/get-started/introduction
- **API base URL:** `https://api.dataforb2b.ai`

## Authentication

### API Key

Custom header authentication using the provider-specific api_key header.

### Credentials

- **User ID:** `userId` · optional · Optional DataForB2B user ID used by user-scoped webhook operations.

[Official authentication documentation](https://docs.dataforb2b.ai/development/authentication)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Endpoints (17 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Add Profiles To Monitor](actions/add-profiles-to-monitor.md) | `POST /webhooks/profiles` | [docs](https://docs.dataforb2b.ai/api-reference/webhooks-add-profiles) |
| [Agentic Search](actions/agentic-search.md) | `POST /search/llm` | [docs](https://docs.dataforb2b.ai/api-reference/agent-search) |
| [Categories Typeahead](actions/categories-typeahead.md) | `GET /typeahead/categories` | [docs](https://docs.dataforb2b.ai/api-reference/typeahead-categories) |
| [Companies Typeahead](actions/companies-typeahead.md) | `GET /typeahead/companies` | [docs](https://docs.dataforb2b.ai/api-reference/typeahead-companies) |
| [Create Webhook Subscription](actions/create-webhook-subscription.md) | `POST /webhooks` | [docs](https://docs.dataforb2b.ai/api-reference/webhooks-create) |
| [Delete Webhook Subscription](actions/delete-webhook-subscription.md) | `DELETE /webhooks` | [docs](https://docs.dataforb2b.ai/api-reference/webhooks-delete) |
| [Enrich Company](actions/enrich-company.md) | `POST /enrich/company` | [docs](https://docs.dataforb2b.ai/api-reference/enrich-company) |
| [Enrich Profile](actions/enrich-profile.md) | `POST /enrich/profile` | [docs](https://docs.dataforb2b.ai/api-reference/enrich-profile) |
| [Get Account](actions/get-account.md) | `GET /account` | [docs](https://docs.dataforb2b.ai/api-reference/account) |
| [Get Webhook Subscription](actions/get-webhook-subscription.md) | `GET /webhooks` | [docs](https://docs.dataforb2b.ai/api-reference/webhooks-get) |
| [Industries Typeahead](actions/industries-typeahead.md) | `GET /typeahead/industries` | [docs](https://docs.dataforb2b.ai/api-reference/typeahead-industries) |
| [List Webhook Events](actions/list-webhook-events.md) | `GET /webhooks/events` | [docs](https://docs.dataforb2b.ai/api-reference/webhooks-events) |
| [Locations Typeahead](actions/locations-typeahead.md) | `GET /typeahead/locations` | [docs](https://docs.dataforb2b.ai/api-reference/typeahead-locations) |
| [Remove Profiles From Monitoring](actions/remove-profiles-from-monitoring.md) | `DELETE /webhooks/profiles` | [docs](https://docs.dataforb2b.ai/api-reference/webhooks-remove-profiles) |
| [Search Companies](actions/search-companies.md) | `POST /search/companies` | [docs](https://docs.dataforb2b.ai/api-reference/search-company) |
| [Search People](actions/search-people.md) | `POST /search/people` | [docs](https://docs.dataforb2b.ai/api-reference/search-people) |
| [Text To Filters](actions/text-to-filters.md) | `POST /search/llm/filters` | [docs](https://docs.dataforb2b.ai/api-reference/text-to-filters) |
