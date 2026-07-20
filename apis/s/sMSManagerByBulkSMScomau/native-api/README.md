# SMS Manager by BulkSMS.com.au: Native API Reference

A consolidated summary of SMS Manager by BulkSMS.com.au's API configuration and 39 documented operations, with links to official documentation.

- **Official docs:** https://smsmanager.com.au/v2/api_docs
- **OpenAPI specification:** https://smsmanager.com.au/v2/api/openapi.php
- **API base URL:** `https://smsmanager.com.au/v2/api`

## Authentication

### API Key

Authenticate SMS Manager REST API requests with a provider-native API key sent as a Bearer token in the Authorization header.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://smsmanager.com.au/v2/api_docs)

## API conventions

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |

Responses from this API use JSON. Response data is read from `data`.

## Retry behavior

Retry responses with status codes `429,500,502,503,504`. Wait 1000 ms before the first retry. Stop after 3 attempts. Multiply the delay by 2 after each failed attempt.

## Endpoints (39 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Export Contacts](actions/export-contacts.md) | `GET /contacts/export` | [docs](https://smsmanager.com.au/v2/api_docs) |
| [Export Message History](actions/export-message-history.md) | `GET /messages/export` | [docs](https://smsmanager.com.au/v2/api_docs) |
| [Get Account Settings](actions/get-account-settings.md) | `GET /account/settings` | [docs](https://smsmanager.com.au/v2/api_docs) |
| [Get Auto Top-Up Settings](actions/get-auto-top-up-settings.md) | `GET /autotopup/settings` | [docs](https://smsmanager.com.au/v2/api_docs) |
| [Get Automation Subscription](actions/get-automation-subscription.md) | `GET /automations/subscriptions/:id` | [docs](https://smsmanager.com.au/v2/api_docs) |
| [Get Available Permissions](actions/get-available-permissions.md) | `GET /account/permissions` | [docs](https://smsmanager.com.au/v2/api_docs) |
| [Get Blocked Number](actions/get-blocked-number.md) | `GET /blocked_numbers/:blocked_number_id` | [docs](https://smsmanager.com.au/v2/api_docs) |
| [Get Chat Message History](actions/get-chat-message-history.md) | `GET /chats/history` | [docs](https://smsmanager.com.au/v2/api_docs) |
| [Get Client Configuration](actions/get-client-configuration.md) | `GET /config` | [docs](https://smsmanager.com.au/v2/api_docs) |
| [Get Contact](actions/get-contact.md) | `GET /contacts/:id` | [docs](https://smsmanager.com.au/v2/api_docs) |
| [Get Group](actions/get-group.md) | `GET /groups/:id` | [docs](https://smsmanager.com.au/v2/api_docs) |
| [Get Keyword](actions/get-keyword.md) | `GET /interactive/:id` | [docs](https://smsmanager.com.au/v2/api_docs) |
| [Get Message](actions/get-message.md) | `GET /messages/:id` | [docs](https://smsmanager.com.au/v2/api_docs) |
| [Get Message Details](actions/get-message-details.md) | `GET /messages/:id/details` | [docs](https://smsmanager.com.au/v2/api_docs) |
| [Get Message History](actions/get-message-history.md) | `GET /messages` | [docs](https://smsmanager.com.au/v2/api_docs) |
| [Get Message Recipients](actions/get-message-recipients.md) | `GET /messages/:id/recipients` | [docs](https://smsmanager.com.au/v2/api_docs) |
| [Get Message Replies](actions/get-message-replies.md) | `GET /messages/:id/replies` | [docs](https://smsmanager.com.au/v2/api_docs) |
| [Get Message Statistics](actions/get-message-statistics.md) | `GET /messages/stats` | [docs](https://smsmanager.com.au/v2/api_docs) |
| [Get My Pending Invitations](actions/get-my-pending-invitations.md) | `GET /account/my-invitations` | [docs](https://smsmanager.com.au/v2/api_docs) |
| [Get Payment Details](actions/get-payment-details.md) | `GET /billing/payment` | [docs](https://smsmanager.com.au/v2/api_docs) |
| [Get Sample Automation Event Data](actions/get-sample-automation-event-data.md) | `GET /automations/samples/:event_type` | [docs](https://smsmanager.com.au/v2/api_docs) |
| [Get Stored Payment Cards](actions/get-stored-payment-cards.md) | `GET /cards` | [docs](https://smsmanager.com.au/v2/api_docs) |
| [List Accessible Accounts](actions/list-accessible-accounts.md) | `GET /account/accessible` | [docs](https://smsmanager.com.au/v2/api_docs) |
| [List Automation Subscriptions](actions/list-automation-subscriptions.md) | `GET /automations/subscriptions` | [docs](https://smsmanager.com.au/v2/api_docs) |
| [List Blocked Numbers](actions/list-blocked-numbers.md) | `GET /blocked_numbers` | [docs](https://smsmanager.com.au/v2/api_docs) |
| [List Chat Conversations](actions/list-chat-conversations.md) | `GET /chats` | [docs](https://smsmanager.com.au/v2/api_docs) |
| [List Contacts](actions/list-contacts.md) | `GET /contacts` | [docs](https://smsmanager.com.au/v2/api_docs) |
| [List Credit Packages](actions/list-credit-packages.md) | `GET /billing/packages` | [docs](https://smsmanager.com.au/v2/api_docs) |
| [List Credit Purchase History](actions/list-credit-purchase-history.md) | `GET /billing/history` | [docs](https://smsmanager.com.au/v2/api_docs) |
| [List Custom Contact Fields](actions/list-custom-contact-fields.md) | `GET /contact-fields` | [docs](https://smsmanager.com.au/v2/api_docs) |
| [List Group Contacts](actions/list-group-contacts.md) | `GET /groups/:id/contacts` | [docs](https://smsmanager.com.au/v2/api_docs) |
| [List Groups](actions/list-groups.md) | `GET /groups` | [docs](https://smsmanager.com.au/v2/api_docs) |
| [List Incoming Messages](actions/list-incoming-messages.md) | `GET /messages/incoming` | [docs](https://smsmanager.com.au/v2/api_docs) |
| [List Keywords](actions/list-keywords.md) | `GET /interactive` | [docs](https://smsmanager.com.au/v2/api_docs) |
| [List Pending Invitations](actions/list-pending-invitations.md) | `GET /account/invitations` | [docs](https://smsmanager.com.au/v2/api_docs) |
| [List Shared Accounts](actions/list-shared-accounts.md) | `GET /account/shared` | [docs](https://smsmanager.com.au/v2/api_docs) |
| [List Team Members](actions/list-team-members.md) | `GET /account/members` | [docs](https://smsmanager.com.au/v2/api_docs) |
| [Verify API Key](actions/verify-api-key.md) | `GET /auth/verify` | [docs](https://smsmanager.com.au/v2/api_docs) |
| [View Invoice](actions/view-invoice.md) | `GET /billing/invoice/:invoice_id` | [docs](https://smsmanager.com.au/v2/api_docs) |
