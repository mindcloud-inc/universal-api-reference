# DecisionVault: Native API Reference

A consolidated summary of DecisionVault's API configuration and 17 documented operations, with links to official documentation.

- **Official docs:** https://docs.decisionvault.com/
- **API base URL:** `https://api.decisionvault.com/v1`

## Authentication

### OAuth2

Register an OAuth application with the provider to obtain client credentials and configure its redirect URI.

1. Send the user to https://app.decisionvault.com/oauth/authorize to approve access.
2. Exchange the returned authorization code with a POST request to https://app.decisionvault.com/oauth/token.
3. Send the resulting access token as `Authorization: Bearer <accessToken>` on API requests.


The flow supports refresh tokens. Refresh expired access tokens with a POST request to https://app.decisionvault.com/oauth/token.

[Official authentication documentation](https://docs.decisionvault.com/authentication-1612114m0)

### API Key

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://docs.decisionvault.com/authentication-1612114m0)

## API conventions

The next-page cursor is read from `next`.

## Pagination

Use `page_size` in the query string to set the page size (default 100; accepted range 1–200). Use `page` in the query string to choose the page; numbering starts at 1. Follow the complete next-page URL returned by the API.

## Endpoints (17 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Matter](actions/create-matter.md) | `POST /matters/create` | [docs](https://docs.decisionvault.com/create-matter-21684966e0.md) |
| [Create Webhook Subscription](actions/create-webhook-subscription.md) | `POST /subscriptions` | [docs](https://docs.decisionvault.com/create-webhook-subscription-21684970e0.md) |
| [Delete Webhook Subscription](actions/delete-webhook-subscription.md) | `DELETE /subscriptions/:subscription_id` | [docs](https://docs.decisionvault.com/delete-webhook-subscription-21684971e0.md) |
| [Get Document](actions/get-document.md) | `GET /documents/:document_id` | [docs](https://docs.decisionvault.com/get-single-document-21747687e0.md) |
| [Get Event](actions/get-event.md) | `GET /events/:event_id` | [docs](https://docs.decisionvault.com/get-single-event-21684968e0.md) |
| [Get Matter](actions/get-matter.md) | `GET /matters/:matter_id` | [docs](https://docs.decisionvault.com/get-single-matter-21684962e0.md) |
| [Get Questionnaire](actions/get-questionnaire.md) | `GET /questionnaires/:questionnaire_id` | [docs](https://docs.decisionvault.com/get-single-questionnaire-21684959e0.md) |
| [Get User](actions/get-user.md) | `GET /users/:user_id` | [docs](https://docs.decisionvault.com/get-single-user-21684969e0.md) |
| [List Assets for Matter](actions/list-assets-for-matter.md) | `GET /matters/:matter_id/assets` | [docs](https://docs.decisionvault.com/get-assets-for-a-matter-21684963e0.md) |
| [List Clients for Matter](actions/list-clients-for-matter.md) | `GET /matters/:matter_id/clients` | [docs](https://docs.decisionvault.com/get-clients-for-a-matter-21684965e0.md) |
| [List Contacts for Matter](actions/list-contacts-for-matter.md) | `GET /matters/:matter_id/contacts` | [docs](https://docs.decisionvault.com/get-contacts-for-a-matter-21684964e0.md) |
| [List Documents for Matter](actions/list-documents-for-matter.md) | `GET /matters/:matter_id/documents` | [docs](https://docs.decisionvault.com/get-documents-for-matter-21745356e0.md) |
| [List Events](actions/list-events.md) | `GET /events` | [docs](https://docs.decisionvault.com/get-events-21684967e0.md) |
| [List Financial Categories](actions/list-financial-categories.md) | `GET /financial-categories` | [docs](https://docs.decisionvault.com/get-financial-categories-21684960e0.md) |
| [List Financial Documents for Matter](actions/list-financial-documents-for-matter.md) | `GET /matters/:matter_id/financial-documents` | [docs](https://docs.decisionvault.com/get-financial-documents-for-matter-21745392e0.md) |
| [List Matters](actions/list-matters.md) | `GET /matters` | [docs](https://docs.decisionvault.com/get-matters-21684961e0.md) |
| [List Questionnaires](actions/list-questionnaires.md) | `GET /questionnaires` | [docs](https://docs.decisionvault.com/get-questionnaires-21684958e0.md) |
