# Sakari SMS: Native API Reference

A consolidated summary of Sakari SMS's API configuration and 40 documented operations, with links to official documentation.

- **Official docs:** https://developer.sakari.io/api-reference
- **OpenAPI specification:** https://developer.sakari.io/api-reference/generated.yaml
- **API base URL:** `https://api.sakari.io`

## Authentication

### OAuth2 Client Credentials

Authenticate with Sakari using OAuth2 client credentials.

### Credentials

- **Account ID:** `accountId` · required · Your Sakari account ID from the API Credentials section.

Register an OAuth application with the provider to obtain client credentials and configure its redirect URI.

1. Exchange the returned authorization code with a POST request to https://api.sakari.io/oauth2/token.
2. Send the resulting access token as `Authorization: Bearer <accessToken>` on API requests.


A machine-to-machine flow is configured.

[Official authentication documentation](https://developer.sakari.io/quickstart#step-1-authenticate)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON. Response data is read from `data`.

## Pagination

Use `limit` in the query string to set the page size (accepted range 1–100). Use `offset` in the query string as the record offset; numbering starts at 0.

## Endpoints (40 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Activate Existing Form](actions/activate-existing-form.md) | `PUT /v1/accounts/:accountId/forms/:formId/activate` | [docs](https://developer.sakari.io/api-reference/forms/activate-an-existing-form) |
| [Close Conversation](actions/close-conversation.md) | `PUT /v1/accounts/:accountId/conversations/:conversationId/close` | [docs](https://developer.sakari.io/api-reference/conversations/closes-a-conversation) |
| [Create And Execute Campaign](actions/create-and-execute-campaign.md) | `POST /v1/accounts/:accountId/quickcampaigns` | [docs](https://developer.sakari.io/api-reference/campaigns/create-and-execute-a-campaign) |
| [Create Campaign](actions/create-campaign.md) | `POST /v1/accounts/:accountId/campaigns` | [docs](https://developer.sakari.io/api-reference/campaigns/create-campaign) |
| [Create Contact](actions/create-contact.md) | `POST /v1/accounts/:accountId/contacts` | [docs](https://developer.sakari.io/api-reference/contacts/create-contact) |
| [Create Lead Form](actions/create-lead-form.md) | `POST /v1/accounts/:accountId/forms` | [docs](https://developer.sakari.io/api-reference/forms/create-lead-form) |
| [Create Template](actions/create-template.md) | `POST /v1/accounts/:accountId/templates` | [docs](https://developer.sakari.io/api-reference/templates/create-template) |
| [Deactivate Existing Form](actions/deactivate-existing-form.md) | `PUT /v1/accounts/:accountId/forms/:formId/deactivate` | [docs](https://developer.sakari.io/api-reference/forms/deactivate-an-existing-form) |
| [Delete Campaign](actions/delete-campaign.md) | `DELETE /v1/accounts/:accountId/campaigns/:campaignId` | [docs](https://developer.sakari.io/api-reference/campaigns/deletes-a-campaign) |
| [Delete Contact](actions/delete-contact.md) | `DELETE /v1/accounts/:accountId/contacts/:contactId` | [docs](https://developer.sakari.io/api-reference/contacts/deletes-a-contact) |
| [Delete Lead Form](actions/delete-lead-form.md) | `DELETE /v1/accounts/:accountId/forms/:formId` | [docs](https://developer.sakari.io/api-reference/forms/delete-a-lead-form) |
| [Delete Template](actions/delete-template.md) | `DELETE /v1/accounts/:accountId/templates/:templateId` | [docs](https://developer.sakari.io/api-reference/templates/deletes-a-template) |
| [Get Account](actions/get-account.md) | `GET /v1/accounts/:accountId` | [docs](https://developer.sakari.io/api-reference/accounts/fetch-account) |
| [Get Account Balance](actions/get-account-balance.md) | `GET /v1/accounts/:accountId/balance` | [docs](https://developer.sakari.io/api-reference/accounts/fetch-account-balance) |
| [Get Campaign by ID](actions/get-campaign-by-id.md) | `GET /v1/accounts/:accountId/campaigns/:campaignId` | [docs](https://developer.sakari.io/api-reference/campaigns/fetch-campaign-by-id) |
| [Get Contact by ID](actions/get-contact-by-id.md) | `GET /v1/accounts/:accountId/contacts/:contactId` | [docs](https://developer.sakari.io/api-reference/contacts/fetch-contact-by-id) |
| [Get Conversation by ID](actions/get-conversation-by-id.md) | `GET /v1/accounts/:accountId/conversations/:conversationId` | [docs](https://developer.sakari.io/api-reference/conversations/fetch-conversation-by-id) |
| [Get Lead Form](actions/get-lead-form.md) | `GET /v1/accounts/:accountId/forms/:formId` | [docs](https://developer.sakari.io/api-reference/forms/fetch-lead-form-info) |
| [Get Lead Form Analytic Data](actions/get-lead-form-analytic-data.md) | `GET /v1/accounts/:accountId/forms/:formId/analytics` | [docs](https://developer.sakari.io/api-reference/forms/fetch-lead-form-analytic-data) |
| [Get Lead Form Conversion Data](actions/get-lead-form-conversion-data.md) | `GET /v1/accounts/:accountId/forms/:formId/conversions` | [docs](https://developer.sakari.io/api-reference/forms/fetch-lead-form-conversion-data) |
| [Get Link by ID](actions/get-link-by-id.md) | `GET /v1/accounts/:accountId/links/:linkId` | [docs](https://developer.sakari.io/api-reference/links/fetch-link-by-id) |
| [Get Message by ID](actions/get-message-by-id.md) | `GET /v1/accounts/:accountId/messages/:messageId` | [docs](https://developer.sakari.io/api-reference/messages/fetch-message-by-id) |
| [Get Template by ID](actions/get-template-by-id.md) | `GET /v1/accounts/:accountId/templates/:templateId` | [docs](https://developer.sakari.io/api-reference/templates/fetch-template-by-id) |
| [List Active Webhooks](actions/list-active-webhooks.md) | `GET /v1/accounts/:accountId/webhooks` | [docs](https://developer.sakari.io/api-reference/webhooks/fetch-active-webhooks) |
| [List Available Phone Numbers](actions/list-available-phone-numbers.md) | `GET /v1/accounts/:accountId/availablephonenumbers` | [docs](https://developer.sakari.io/api-reference/availablephonenumbers/check-all-available-phone-numbers) |
| [List Campaigns](actions/list-campaigns.md) | `GET /v1/accounts/:accountId/campaigns` | [docs](https://developer.sakari.io/api-reference/campaigns/fetch-campaigns) |
| [List Contacts](actions/list-contacts.md) | `GET /v1/accounts/:accountId/contacts` | [docs](https://developer.sakari.io/api-reference/contacts/fetch-contacts) |
| [List Conversations](actions/list-conversations.md) | `GET /v1/accounts/:accountId/conversations` | [docs](https://developer.sakari.io/api-reference/conversations/fetch-conversations) |
| [List Lead Form Templates](actions/list-lead-form-templates.md) | `GET /v1/accounts/:accountId/forms/templates` | [docs](https://developer.sakari.io/api-reference/forms/fetch-all-lead-form-templates) |
| [List Lead Forms](actions/list-lead-forms.md) | `GET /v1/accounts/:accountId/forms` | [docs](https://developer.sakari.io/api-reference/forms/fetch-all-lead-forms) |
| [List Link Sources](actions/list-link-sources.md) | `GET /v1/accounts/:accountId/links/:linkId/sources` | [docs](https://developer.sakari.io/api-reference/links/fetch-link-sources) |
| [List Links](actions/list-links.md) | `GET /v1/accounts/:accountId/links` | [docs](https://developer.sakari.io/api-reference/links/fetch-links) |
| [List Messages](actions/list-messages.md) | `GET /v1/accounts/:accountId/messages` | [docs](https://developer.sakari.io/api-reference/messages/fetch-messages) |
| [List Templates](actions/list-templates.md) | `GET /v1/accounts/:accountId/templates` | [docs](https://developer.sakari.io/api-reference/templates/fetch-templates) |
| [Send Messages](actions/send-messages.md) | `POST /v1/accounts/:accountId/messages` | [docs](https://developer.sakari.io/api-reference/messages/send-messages) |
| [Subscribe To Message Events](actions/subscribe-to-message-events.md) | `POST /v1/accounts/:accountId/webhooks` | [docs](https://developer.sakari.io/api-reference/webhooks/subscribe-to-message-events) |
| [Update Campaign](actions/update-campaign.md) | `PUT /v1/accounts/:accountId/campaigns/:campaignId` | [docs](https://developer.sakari.io/api-reference/campaigns/updates-a-campaign) |
| [Update Contact](actions/update-contact.md) | `PUT /v1/accounts/:accountId/contacts/:contactId` | [docs](https://developer.sakari.io/api-reference/contacts/updates-a-contact) |
| [Update Lead Form](actions/update-lead-form.md) | `PUT /v1/accounts/:accountId/forms/:formId` | [docs](https://developer.sakari.io/api-reference/forms/update-lead-form) |
| [Update Template](actions/update-template.md) | `PUT /v1/accounts/:accountId/templates/:templateId` | [docs](https://developer.sakari.io/api-reference/templates/updates-a-template) |
