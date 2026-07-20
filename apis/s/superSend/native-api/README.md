# SuperSend: Native API Reference

A consolidated summary of SuperSend's API configuration and 57 documented operations, with links to official documentation.

- **Official docs:** https://docs.supersend.io/docs/v2-api
- **OpenAPI specification:** https://api.supersend.io/v2/openapi.json
- **API base URL:** `https://api.supersend.io/v2`

## Authentication

### API Key

Authenticate with a SuperSend API key.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://docs.supersend.io/docs/authentication)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

Responses from this API use JSON. Response data is read from `data`.

## Pagination

Use `limit` in the query string to set the page size (default 50). Use `offset` in the query string as the record offset; numbering starts at 0.

## Retry behavior

Retry responses with status codes `500,503`. Wait 1000 ms before the first retry. Stop after 3 attempts. Multiply the delay by 2 after each failed attempt.

## Endpoints (57 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Assign Label to Contact Profile](actions/assign-label-to-contact-profile.md) | `POST /contacts/{id}/profile-labels` | [docs](https://docs.supersend.io/docs/contact) |
| [Bulk Import Contacts](actions/bulk-import-contacts.md) | `POST /contacts/bulk` | [docs](https://docs.supersend.io/docs/contact) |
| [Create Campaign](actions/create-campaign.md) | `POST /campaigns` | [docs](https://docs.supersend.io/docs/campaign) |
| [Create Campaign Category](actions/create-campaign-category.md) | `POST /campaign-categories` | [docs](https://docs.supersend.io/docs/campaign-category) |
| [Create Contact](actions/create-contact.md) | `POST /contacts` | [docs](https://docs.supersend.io/docs/contact) |
| [Create Placement Test](actions/create-placement-test.md) | `POST /placement-tests` | [docs](https://docs.supersend.io/docs/placement-test) |
| [Create Team](actions/create-team.md) | `POST /teams` | [docs](https://docs.supersend.io/docs/team) |
| [Delete Campaign Category](actions/delete-campaign-category.md) | `DELETE /campaign-categories/{id}` | [docs](https://docs.supersend.io/docs/campaign-category) |
| [Delete Contact](actions/delete-contact.md) | `DELETE /contacts/{id}` | [docs](https://docs.supersend.io/docs/contact) |
| [Delete Contact by Identifier](actions/delete-contact-by-identifier.md) | `DELETE /contacts` | [docs](https://docs.supersend.io/docs/contact) |
| [Export Placement Tests](actions/export-placement-tests.md) | `POST /placement-tests/export` | [docs](https://docs.supersend.io/docs/placement-test) |
| [Get Campaign](actions/get-campaign.md) | `GET /campaigns/{id}` | [docs](https://docs.supersend.io/docs/campaign) |
| [Get Campaign Sequence](actions/get-campaign-sequence.md) | `GET /campaigns/{id}/sequence` | [docs](https://docs.supersend.io/docs/campaign) |
| [Get Capacity Summary](actions/get-capacity-summary.md) | `GET /intelligence/capacity-summary` | [docs](https://api.supersend.io/v2/openapi.json) |
| [Get Contact](actions/get-contact.md) | `GET /contacts/{id}` | [docs](https://docs.supersend.io/docs/contact) |
| [Get Conversation](actions/get-conversation.md) | `GET /conversations/{id}` | [docs](https://docs.supersend.io/docs/conversation) |
| [Get Conversation Messages](actions/get-conversation-messages.md) | `GET /conversations/{id}/messages` | [docs](https://docs.supersend.io/docs/conversation) |
| [Get Deliverability Summary](actions/get-deliverability-summary.md) | `GET /intelligence/deliverability-summary` | [docs](https://api.supersend.io/v2/openapi.json) |
| [Get Domain](actions/get-domain.md) | `GET /domains/{id}` | [docs](https://docs.supersend.io/docs/managed-domain) |
| [Get Domain Health Summary](actions/get-domain-health-summary.md) | `GET /intelligence/domain-health-summary` | [docs](https://api.supersend.io/v2/openapi.json) |
| [Get Event](actions/get-event.md) | `GET /events/{id}` | [docs](https://docs.supersend.io/docs/event) |
| [Get Health Check](actions/get-health-check.md) | `GET /health` | [docs](https://docs.supersend.io/docs/v2-api) |
| [Get Outbound Summary](actions/get-outbound-summary.md) | `GET /intelligence/outbound-summary` | [docs](https://api.supersend.io/v2/openapi.json) |
| [Get Placement Test](actions/get-placement-test.md) | `GET /placement-tests/{id}` | [docs](https://docs.supersend.io/docs/placement-test) |
| [Get Sender](actions/get-sender.md) | `GET /senders/{id}` | [docs](https://docs.supersend.io/docs/sender) |
| [Get Sender Health Summary](actions/get-sender-health-summary.md) | `GET /intelligence/sender-health-summary` | [docs](https://api.supersend.io/v2/openapi.json) |
| [Get Team](actions/get-team.md) | `GET /teams/{id}` | [docs](https://docs.supersend.io/docs/team) |
| [Get Team Cost Allocation](actions/get-team-cost-allocation.md) | `GET /billing/team-usage` | [docs](https://docs.supersend.io/docs/v2-api) |
| [Get Team Usage](actions/get-team-usage.md) | `GET /teams/{id}/usage` | [docs](https://docs.supersend.io/docs/team) |
| [Get Webhook Delivery](actions/get-webhook-delivery.md) | `GET /webhooks/{id}/deliveries/{deliveryId}` | [docs](https://docs.supersend.io/docs/webhooks) |
| [List Announcements](actions/list-announcements.md) | `GET /announcements` | [docs](https://docs.supersend.io/docs/v2-api) |
| [List Campaign Categories](actions/list-campaign-categories.md) | `GET /campaign-categories` | [docs](https://docs.supersend.io/docs/campaign-category) |
| [List Campaigns](actions/list-campaigns.md) | `GET /campaigns` | [docs](https://docs.supersend.io/docs/campaign) |
| [List Contact Profile Labels](actions/list-contact-profile-labels.md) | `GET /contacts/{id}/profile-labels` | [docs](https://docs.supersend.io/docs/contact) |
| [List Contacts](actions/list-contacts.md) | `GET /contacts` | [docs](https://docs.supersend.io/docs/contact) |
| [List Conversations](actions/list-conversations.md) | `GET /conversations` | [docs](https://docs.supersend.io/docs/conversation) |
| [List Domains](actions/list-domains.md) | `GET /domains` | [docs](https://docs.supersend.io/docs/managed-domain) |
| [List Events](actions/list-events.md) | `GET /events` | [docs](https://docs.supersend.io/docs/event) |
| [List Placement Tests](actions/list-placement-tests.md) | `GET /placement-tests` | [docs](https://docs.supersend.io/docs/placement-test) |
| [List Senders](actions/list-senders.md) | `GET /senders` | [docs](https://docs.supersend.io/docs/sender) |
| [List Teams](actions/list-teams.md) | `GET /teams` | [docs](https://docs.supersend.io/docs/team) |
| [List Webhook Deliveries](actions/list-webhook-deliveries.md) | `GET /webhooks/{id}/deliveries` | [docs](https://docs.supersend.io/docs/webhooks) |
| [List Webhooks](actions/list-webhooks.md) | `GET /webhooks` | [docs](https://docs.supersend.io/docs/webhooks) |
| [Purchase Domains](actions/purchase-domains.md) | `POST /domains/purchase` | [docs](https://docs.supersend.io/docs/managed-domain) |
| [Purchase Domains and Mailboxes](actions/purchase-domains-and-mailboxes.md) | `POST /domains/purchase-with-mailboxes` | [docs](https://docs.supersend.io/docs/managed-domain) |
| [Purchase Mailboxes](actions/purchase-mailboxes.md) | `POST /mailboxes/purchase` | [docs](https://docs.supersend.io/docs/managed-mailbox) |
| [Remove Contact Profile Label](actions/remove-contact-profile-label.md) | `DELETE /contacts/{id}/profile-labels/{labelId}` | [docs](https://docs.supersend.io/docs/contact) |
| [Retry Webhook Delivery](actions/retry-webhook-delivery.md) | `POST /webhooks/{id}/deliveries/{deliveryId}/retry` | [docs](https://docs.supersend.io/docs/webhooks) |
| [Send Conversation Message](actions/send-conversation-message.md) | `POST /conversations/{id}/messages` | [docs](https://docs.supersend.io/docs/conversation) |
| [Update Campaign](actions/update-campaign.md) | `PATCH /campaigns/{id}` | [docs](https://docs.supersend.io/docs/campaign) |
| [Update Campaign Category](actions/update-campaign-category.md) | `PATCH /campaign-categories` | [docs](https://docs.supersend.io/docs/campaign-category) |
| [Update Campaign Sequence](actions/update-campaign-sequence.md) | `PATCH /campaigns/{id}/sequence` | [docs](https://docs.supersend.io/docs/campaign) |
| [Update Contact](actions/update-contact.md) | `PATCH /contacts/{id}` | [docs](https://docs.supersend.io/docs/contact) |
| [Update Conversation](actions/update-conversation.md) | `PATCH /conversations/{id}` | [docs](https://docs.supersend.io/docs/conversation) |
| [Update Sender](actions/update-sender.md) | `PATCH /senders/{id}` | [docs](https://docs.supersend.io/docs/sender) |
| [Update Team](actions/update-team.md) | `PATCH /teams/{id}` | [docs](https://docs.supersend.io/docs/team) |
| [Verify Email (SMTP)](actions/verify-email-smtp.md) | `POST /email-validation/verify` | [docs](https://docs.supersend.io/docs/email-validation) |
