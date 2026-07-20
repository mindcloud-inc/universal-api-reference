# Paycove: Native API Reference

A consolidated summary of Paycove's API configuration and 34 documented operations, with links to official documentation.

- **Official docs:** https://docs.paycove.io/
- **API base URL:** `https://paycove.io/api/v1`

## Authentication

### OAuth 2.0

### Credentials

- **Client Secret:** `clientSecret` · required · Paycove OAuth client secret from the API Clients page.
- **Client ID:** `clientId` · required · Paycove OAuth client ID from the API Clients page.

Register an OAuth application with the provider to obtain client credentials and configure its redirect URI.

1. Send the user to https://paycove.io/oauth/authorize to approve access.
2. Exchange the returned authorization code with a POST request to https://paycove.io/oauth/token.
3. Send the resulting access token as `Authorization: Bearer <accessToken>` on API requests.


The flow supports refresh tokens. Refresh expired access tokens with a POST request to https://paycove.io/oauth/token.

[Official authentication documentation](https://docs.paycove.io/#203bf2bc-dfeb-4ace-8e2f-0f006efc8dd1)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON. Response data is read from `data`.

## Pagination

Use `limit` in the query string to set the page size (default 50; maximum 100). Use `page` in the query string to choose the page; numbering starts at 1.

## Endpoints (34 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Account](actions/create-account.md) | `POST accounts` | [docs](https://docs.paycove.io/) |
| [Create Checkout Session](actions/create-checkout-session.md) | `POST https://paycove.io/api/checkout/:aid` | [docs](https://docs.paycove.io/) |
| [Create Deal](actions/create-deal.md) | `POST deals/with-relations` | [docs](https://docs.paycove.io/) |
| [Create Deal Scheduled Payments](actions/create-deal-scheduled-payments.md) | `POST add-scheduled-payments/:deal_id` | [docs](https://docs.paycove.io/) |
| [Create Fee](actions/create-fee.md) | `POST deals/:crm_deal_id/fees` | [docs](https://docs.paycove.io/) |
| [Create Product](actions/create-product.md) | `POST products` | [docs](https://docs.paycove.io/) |
| [Create Webhook Subscription](actions/create-webhook-subscription.md) | `POST hooks` | [docs](https://docs.paycove.io/) |
| [Delete Contact](actions/delete-contact.md) | `DELETE contacts/:id` | [docs](https://docs.paycove.io/) |
| [Delete Deal](actions/delete-deal.md) | `DELETE deals/:id` | [docs](https://docs.paycove.io/) |
| [Delete Organization](actions/delete-organization.md) | `DELETE organizations/:id` | [docs](https://docs.paycove.io/) |
| [Delete Product](actions/delete-product.md) | `DELETE products/:product_id` | [docs](https://docs.paycove.io/) |
| [Delete Webhook Subscription](actions/delete-webhook-subscription.md) | `DELETE hooks` | [docs](https://docs.paycove.io/) |
| [Get Application Status](actions/get-application-status.md) | `GET https://paycove.io/gateway-application-status/:unique_account_id` | [docs](https://docs.paycove.io/) |
| [Get Contact Details](actions/get-contact-details.md) | `GET contacts/:id` | [docs](https://docs.paycove.io/) |
| [Get Current User](actions/get-current-user.md) | `GET user` | [docs](https://docs.paycove.io/) |
| [Get Deal Details](actions/get-deal-details.md) | `GET deals/:id` | [docs](https://docs.paycove.io/) |
| [Get Organization Details](actions/get-organization-details.md) | `GET organizations/:id` | [docs](https://docs.paycove.io/) |
| [Get Product](actions/get-product.md) | `GET products/:product_id` | [docs](https://docs.paycove.io/) |
| [Invite Users](actions/invite-users.md) | `POST accounts/invite-users` | [docs](https://docs.paycove.io/) |
| [Issue Refund](actions/issue-refund.md) | `POST issue-refund` | [docs](https://docs.paycove.io/) |
| [Legal Accept](actions/legal-accept.md) | `POST accounts/legal-accept` | [docs](https://docs.paycove.io/) |
| [List Contacts](actions/list-contacts.md) | `GET contacts` | [docs](https://docs.paycove.io/) |
| [List Deal Scheduled Payments](actions/list-deal-scheduled-payments.md) | `GET scheduled-payments/:deal_id` | [docs](https://docs.paycove.io/) |
| [List Deals](actions/list-deals.md) | `GET deals` | [docs](https://docs.paycove.io/) |
| [List Organizations](actions/list-organizations.md) | `GET organizations` | [docs](https://docs.paycove.io/) |
| [List Products](actions/list-products.md) | `GET products` | [docs](https://docs.paycove.io/) |
| [List Scheduled Payments](actions/list-scheduled-payments.md) | `GET scheduled-payments` | [docs](https://docs.paycove.io/) |
| [List Webhooks](actions/list-webhooks.md) | `GET hooks` | [docs](https://docs.paycove.io/) |
| [Reassign To New CRM Deal](actions/reassign-to-new-crm-deal.md) | `PATCH deals/:id/update-crm-deal-id` | [docs](https://docs.paycove.io/) |
| [Start Or Continue Gateway Application](actions/start-or-continue-gateway-application.md) | `GET https://paycove.io/continue-gateway-application/:unique_account_id` | [docs](https://docs.paycove.io/) |
| [Update Contact](actions/update-contact.md) | `PATCH contacts/:id` | [docs](https://docs.paycove.io/) |
| [Update Deal Scheduled Payments](actions/update-deal-scheduled-payments.md) | `PATCH update-scheduled-payments/:deal_id` | [docs](https://docs.paycove.io/) |
| [Update Organization](actions/update-organization.md) | `PATCH organizations/:id` | [docs](https://docs.paycove.io/) |
| [Update Product](actions/update-product.md) | `PATCH products/:product_id` | [docs](https://docs.paycove.io/) |
