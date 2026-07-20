# Clio Grow: Native API Reference

A consolidated summary of Clio Grow's API configuration and 15 documented operations, with links to official documentation.

- **Official docs:** https://docs.developers.clio.com/clio-grow/api-reference/
- **OpenAPI specification:** https://docs.developers.clio.com/clio-grow/api-reference/openapi.yaml
- **API base URL:** `https://api.clio.com/grow`

## Authentication

### OAuth2

Connect a Clio Platform OAuth application for Clio Grow.

### Credentials

- **App Key:** `clientId` · required · Paste the App Key from the Clio Platform Developer Application created for this Clio Grow firm.
- **App Secret:** `clientSecret` · required · Paste the App Secret from the same Clio Platform Developer Application as the App Key.

Register an OAuth application with the provider to obtain client credentials and configure its redirect URI.

1. Send the user to https://auth.api.clio.com/oauth/authorize to approve access.
2. Exchange the returned authorization code with a POST request to https://auth.api.clio.com/oauth/token.
3. Send the resulting access token as `Authorization: Bearer <accessToken>` on API requests.

Requested scopes: `grow_lead_inbox_read grow_lead_inbox_write grow_custom_action_read grow_custom_action_write grow_matter_read grow_matter_note_read grow_matter_note_write grow_contact_read grow_contact_note_read grow_contact_note_write grow_user_read`.

The flow supports refresh tokens. Refresh expired access tokens with a POST request to https://auth.api.clio.com/oauth/token.

[Official authentication documentation](https://docs.developers.clio.com/api-docs/clio-platform/authorization/)

## Pagination

The page size is configurable (default 200; maximum 200). Use `page_token` in the query string as the pagination cursor. Follow the complete next-page URL returned by the API.

## Retry behavior

Retry responses with status codes `429,500`. Wait 1000 ms before the first retry. Stop after 5 attempts. Multiply the delay by 2 after each failed attempt.

## Endpoints (15 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Contact Note](actions/create-contact-note.md) | `POST /contacts/{contact_id}/notes` | [docs](https://docs.developers.clio.com/clio-grow/api-reference/#tag/Contacts/operation/ContactNote%23create) |
| [Create Custom Action](actions/create-custom-action.md) | `POST /custom_actions` | [docs](https://docs.developers.clio.com/clio-grow/api-reference/#tag/Custom-Actions/operation/CustomAction%23create) |
| [Create Inbox Lead](actions/create-inbox-lead.md) | `POST /inbox_leads` | [docs](https://docs.developers.clio.com/clio-grow/api-reference/#tag/Inbox-Leads/operation/InboxLead%23create) |
| [Create Matter Note](actions/create-matter-note.md) | `POST /matters/{matter_id}/notes` | [docs](https://docs.developers.clio.com/clio-grow/api-reference/#tag/Matters/operation/MatterNote%23create) |
| [Get Contact](actions/get-contact.md) | `GET /contacts/{id}` | [docs](https://docs.developers.clio.com/clio-grow/api-reference/#tag/Contacts/operation/Contact%23show) |
| [Get Current User](actions/get-current-user.md) | `GET /users/who_am_i` | [docs](https://docs.developers.clio.com/clio-grow/api-reference/#tag/Users/operation/User%23who_am_i) |
| [Get Inbox Lead](actions/get-inbox-lead.md) | `GET /inbox_leads/{id}` | [docs](https://docs.developers.clio.com/clio-grow/api-reference/#tag/Inbox-Leads/operation/InboxLead%23show) |
| [Get Matter](actions/get-matter.md) | `GET /matters/{id}` | [docs](https://docs.developers.clio.com/clio-grow/api-reference/#tag/Matters/operation/Matter%23show) |
| [List Contact Notes](actions/list-contact-notes.md) | `GET /contacts/{contact_id}/notes` | [docs](https://docs.developers.clio.com/clio-grow/api-reference/#tag/Contacts/operation/ContactNote%23index) |
| [List Contacts](actions/list-contacts.md) | `GET /contacts` | [docs](https://docs.developers.clio.com/clio-grow/api-reference/#tag/Contacts/operation/Contact%23index) |
| [List Custom Actions](actions/list-custom-actions.md) | `GET /custom_actions` | [docs](https://docs.developers.clio.com/clio-grow/api-reference/#tag/Custom-Actions/operation/CustomAction%23index) |
| [List Inbox Leads](actions/list-inbox-leads.md) | `GET /inbox_leads` | [docs](https://docs.developers.clio.com/clio-grow/api-reference/#tag/Inbox-Leads/operation/InboxLead%23index) |
| [List Matter Notes](actions/list-matter-notes.md) | `GET /matters/{matter_id}/notes` | [docs](https://docs.developers.clio.com/clio-grow/api-reference/#tag/Matters/operation/MatterNote%23index) |
| [List Matters](actions/list-matters.md) | `GET /matters` | [docs](https://docs.developers.clio.com/clio-grow/api-reference/#tag/Matters/operation/Matter%23index) |
| [List Users](actions/list-users.md) | `GET /users` | [docs](https://docs.developers.clio.com/clio-grow/api-reference/#tag/Users/operation/User%23index) |
