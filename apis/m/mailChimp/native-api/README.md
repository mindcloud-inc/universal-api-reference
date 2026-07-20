# Mailchimp: Native API Reference

A consolidated summary of Mailchimp's API configuration and 41 documented operations, with links to official documentation.

- **Official docs:** https://mailchimp.com/developer/marketing/api/
- **OpenAPI specification:** https://us22.api.mailchimp.com/schema/3.0/
- **API base URL:** `https://{serverPrefix}.api.mailchimp.com/3.0/`

## Authentication

### OAuth 2

OAuth 2 authentication for accessing Mailchimp Marketing API data on behalf of users.

### Credentials

- **Server Prefix:** `serverPrefix` · required · Mailchimp data center prefix used in API base URL (for example: us19).

Register an OAuth application with the provider to obtain client credentials and configure its redirect URI.

1. Send the user to https://login.mailchimp.com/oauth2/authorize to approve access.
2. Exchange the returned authorization code with a POST request to https://login.mailchimp.com/oauth2/token.
3. Send the resulting access token as `Authorization: Bearer <accessToken>` on API requests.


[Official authentication documentation](https://mailchimp.com/developer/marketing/guides/access-user-data-oauth-2/)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON. Response data is read from `lists`.

## Pagination

Use `count` in the query string to set the page size (default 10; accepted range 1–1000). Use `offset` in the query string as the record offset; numbering starts at 0.

## Sorting

Set the sort field with `sort_field` in the query string. Set the direction separately with `sort_dir`. Use `ASC` for ascending order and `DESC` for descending order. Only one sort field is accepted.

## Retry behavior

Retry responses with status codes `429,500,502,503,504`. Wait 1000 ms before the first retry. Stop after 3 attempts. Multiply the delay by 2 after each failed attempt.

## Endpoints (41 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Add Audience](actions/add-audience.md) | `POST lists` | [docs](https://us22.api.mailchimp.com/schema/3.0/Paths/Lists/Collection.json) |
| [Add Audience Member](actions/add-audience-member.md) | `POST lists/:list_id/members` | [docs](https://us22.api.mailchimp.com/schema/3.0/Paths/Lists/Members/Collection.json) |
| [Add Audience Segment](actions/add-audience-segment.md) | `POST lists/:list_id/segments` | [docs](https://us22.api.mailchimp.com/schema/3.0/Paths/Lists/Segments/Collection.json) |
| [Add Customer](actions/add-customer.md) | `POST ecommerce/stores/:store_id/customers` | [docs](https://mailchimp.com/developer/marketing/api/ecommerce-customers/add-customer/) |
| [Add E-commerce Store](actions/add-e-commerce-store.md) | `POST ecommerce/stores` | [docs](https://us22.api.mailchimp.com/schema/3.0/Paths/Ecommerce/Stores/Collection.json) |
| [Add Merge Field](actions/add-merge-field.md) | `POST lists/:list_id/merge-fields` | [docs](https://us22.api.mailchimp.com/schema/3.0/Paths/Lists/MergeFields/Collection.json) |
| [Archive Audience Member](actions/archive-audience-member.md) | `DELETE lists/:list_id/members/:subscriber_hash` | [docs](https://us22.api.mailchimp.com/schema/3.0/Paths/Lists/Members/Instance.json) |
| [Create Campaign](actions/create-campaign.md) | `POST campaigns` | [docs](https://us22.api.mailchimp.com/schema/3.0/Paths/Campaigns/Collection.json) |
| [Delete Customer](actions/delete-customer.md) | `DELETE ecommerce/stores/:store_id/customers/:customer_id` | [docs](https://mailchimp.com/developer/marketing/api/ecommerce-customers/delete-customer/) |
| [Delete E-commerce Store](actions/delete-e-commerce-store.md) | `DELETE ecommerce/stores/:store_id` | [docs](https://us22.api.mailchimp.com/schema/3.0/Paths/Ecommerce/Stores/Instance.json) |
| [Get Audience](actions/get-audience.md) | `GET lists/:list_id` | [docs](https://us22.api.mailchimp.com/schema/3.0/Paths/Lists/Instance.json) |
| [Get Audience Member](actions/get-audience-member.md) | `GET lists/:list_id/members/:subscriber_hash` | [docs](https://us22.api.mailchimp.com/schema/3.0/Paths/Lists/Members/Instance.json) |
| [Get Audience Segment](actions/get-audience-segment.md) | `GET lists/:list_id/segments/:segment_id` | [docs](https://us22.api.mailchimp.com/schema/3.0/Paths/Lists/Segments/Instance.json) |
| [Get Campaign](actions/get-campaign.md) | `GET campaigns/:campaign_id` | [docs](https://us22.api.mailchimp.com/schema/3.0/Paths/Campaigns/Instance.json) |
| [Get Campaign Content](actions/get-campaign-content.md) | `GET campaigns/:campaign_id/content` | [docs](https://us22.api.mailchimp.com/schema/3.0/Paths/Campaigns/Content/Instance.json) |
| [Get Campaign Report](actions/get-campaign-report.md) | `GET reports/:campaign_id` | [docs](https://us22.api.mailchimp.com/schema/3.0/Paths/Reports/Instance.json) |
| [Get Customer](actions/get-customer.md) | `GET ecommerce/stores/:store_id/customers/:customer_id` | [docs](https://mailchimp.com/developer/marketing/api/ecommerce-customers/get-customer-info/) |
| [Get E-commerce Store](actions/get-e-commerce-store.md) | `GET ecommerce/stores/:store_id` | [docs](https://us22.api.mailchimp.com/schema/3.0/Paths/Ecommerce/Stores/Instance.json) |
| [Get Template](actions/get-template.md) | `GET templates/:template_id` | [docs](https://us22.api.mailchimp.com/schema/3.0/Paths/Templates/Instance.json) |
| [List Audience Members](actions/list-audience-members.md) | `GET lists/:list_id/members` | [docs](https://us22.api.mailchimp.com/schema/3.0/Paths/Lists/Members/Collection.json) |
| [List Audience Segments](actions/list-audience-segments.md) | `GET lists/:list_id/segments` | [docs](https://us22.api.mailchimp.com/schema/3.0/Paths/Lists/Segments/Collection.json) |
| [List Audiences](actions/list-audiences.md) | `GET lists` | [docs](https://mailchimp.com/developer/marketing/api/lists/get-lists-info/) |
| [List Campaigns](actions/list-campaigns.md) | `GET campaigns` | [docs](https://us22.api.mailchimp.com/schema/3.0/Paths/Campaigns/Collection.json) |
| [List Customers](actions/list-customers.md) | `GET ecommerce/stores/:store_id/customers` | [docs](https://mailchimp.com/developer/marketing/api/ecommerce-customers/list-customers/) |
| [List E-commerce Stores](actions/list-e-commerce-stores.md) | `GET ecommerce/stores` | [docs](https://mailchimp.com/developer/marketing/api/ecommerce-stores/list-stores/) |
| [List Member Tags](actions/list-member-tags.md) | `GET lists/:list_id/members/:subscriber_hash/tags` | [docs](https://us22.api.mailchimp.com/schema/3.0/Paths/Lists/Members/Tags.json) |
| [List Merge Fields](actions/list-merge-fields.md) | `GET lists/:list_id/merge-fields` | [docs](https://us22.api.mailchimp.com/schema/3.0/Paths/Lists/MergeFields/Collection.json) |
| [List Reports](actions/list-reports.md) | `GET reports` | [docs](https://us22.api.mailchimp.com/schema/3.0/Paths/Reports/Collection.json) |
| [List Templates](actions/list-templates.md) | `GET templates` | [docs](https://us22.api.mailchimp.com/schema/3.0/Paths/Templates/Collection.json) |
| [Schedule Campaign](actions/schedule-campaign.md) | `POST campaigns/:campaign_id/actions/schedule` | [docs](https://us22.api.mailchimp.com/schema/3.0/Paths/Campaigns/Actions/Schedule.json) |
| [Send Campaign](actions/send-campaign.md) | `POST campaigns/:campaign_id/actions/send` | [docs](https://us22.api.mailchimp.com/schema/3.0/Paths/Campaigns/Actions/Send.json) |
| [Set Campaign Content](actions/set-campaign-content.md) | `PUT campaigns/:campaign_id/content` | [docs](https://us22.api.mailchimp.com/schema/3.0/Paths/Campaigns/Content/Instance.json) |
| [Update Audience](actions/update-audience.md) | `PATCH lists/:list_id` | [docs](https://us22.api.mailchimp.com/schema/3.0/Paths/Lists/Instance.json) |
| [Update Audience Member](actions/update-audience-member.md) | `PATCH lists/:list_id/members/:subscriber_hash` | [docs](https://us22.api.mailchimp.com/schema/3.0/Paths/Lists/Members/Instance.json) |
| [Update Audience Segment](actions/update-audience-segment.md) | `PATCH lists/:list_id/segments/:segment_id` | [docs](https://us22.api.mailchimp.com/schema/3.0/Paths/Lists/Segments/Instance.json) |
| [Update Campaign](actions/update-campaign.md) | `PATCH campaigns/:campaign_id` | [docs](https://us22.api.mailchimp.com/schema/3.0/Paths/Campaigns/Instance.json) |
| [Update Customer](actions/update-customer.md) | `PATCH ecommerce/stores/:store_id/customers/:customer_id` | [docs](https://mailchimp.com/developer/marketing/api/ecommerce-customers/update-customer/) |
| [Update E-commerce Store](actions/update-e-commerce-store.md) | `PATCH ecommerce/stores/:store_id` | [docs](https://us22.api.mailchimp.com/schema/3.0/Paths/Ecommerce/Stores/Instance.json) |
| [Update Member Tags](actions/update-member-tags.md) | `POST lists/:list_id/members/:subscriber_hash/tags` | [docs](https://us22.api.mailchimp.com/schema/3.0/Paths/Lists/Members/Tags.json) |
| [Upsert Audience Member](actions/upsert-audience-member.md) | `PUT lists/:list_id/members/:subscriber_hash` | [docs](https://us22.api.mailchimp.com/schema/3.0/Paths/Lists/Members/Instance.json) |
| [Upsert Customer](actions/upsert-customer.md) | `PUT ecommerce/stores/:store_id/customers/:customer_id` | [docs](https://mailchimp.com/developer/marketing/api/ecommerce-customers/add-or-update-customer/) |
