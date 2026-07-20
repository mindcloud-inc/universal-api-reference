# Seven: Native API Reference

A consolidated summary of Seven's API configuration and 40 documented operations, with links to official documentation.

- **Official docs:** https://docs.seven.io/en
- **API base URL:** `https://gateway.seven.io/api`

## Authentication

### API Key

Connect to seven.io with an API key sent in the X-Api-Key header.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
X-Api-Key: <apiKey>
```

[Official authentication documentation](https://docs.seven.io/en/rest-api/authentication)

## API conventions

Request bodies use URL-encoded form data.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/x-www-form-urlencoded` |

Responses from this API use JSON.

## Endpoints (40 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Contact](actions/create-contact.md) | `POST /contacts` | [docs](https://docs.seven.io/en/rest-api/endpoints/contacts#create-contact) |
| [Create Group](actions/create-group.md) | `POST /groups` | [docs](https://docs.seven.io/en/rest-api/endpoints/groups#create-group) |
| [Create Subaccount](actions/create-subaccount.md) | `POST /subaccounts?action=create` | [docs](https://docs.seven.io/en/rest-api/endpoints/subaccounts#create-subaccount) |
| [Create Webhook](actions/create-webhook.md) | `POST /hooks` | [docs](https://docs.seven.io/en/rest-api/endpoints/webhooks#register-webhook) |
| [Delete Contact](actions/delete-contact.md) | `DELETE /contacts/:id` | [docs](https://docs.seven.io/en/rest-api/endpoints/contacts#delete-contact) |
| [Delete Group](actions/delete-group.md) | `DELETE /groups/:id` | [docs](https://docs.seven.io/en/rest-api/endpoints/groups#delete-group) |
| [Delete Number](actions/delete-number.md) | `DELETE /numbers/active/:number` | [docs](https://docs.seven.io/en/rest-api/endpoints/numbers#delete-number) |
| [Delete SMS](actions/delete-sms.md) | `DELETE /sms` | [docs](https://docs.seven.io/en/rest-api/endpoints/sms#delete-sms) |
| [Delete Subaccount](actions/delete-subaccount.md) | `POST /subaccounts?action=delete` | [docs](https://docs.seven.io/en/rest-api/endpoints/subaccounts#deleting-subaccounts) |
| [Delete Webhook](actions/delete-webhook.md) | `DELETE /hooks` | [docs](https://docs.seven.io/en/rest-api/endpoints/webhooks#delete-webhook) |
| [End Call](actions/end-call.md) | `POST /voice/:call_id/hangup` | [docs](https://docs.seven.io/en/rest-api/endpoints/voice#end-call) |
| [Format Number](actions/format-number.md) | `GET /lookup/format` | [docs](https://docs.seven.io/en/rest-api/endpoints/lookup#format) |
| [Get Active Number](actions/get-active-number.md) | `GET /numbers/active/:number` | [docs](https://docs.seven.io/en/rest-api/endpoints/numbers#get-single-active-number) |
| [Get Balance](actions/get-balance.md) | `GET /balance` | [docs](https://docs.seven.io/en/rest-api/endpoints/account#balance) |
| [Get CNAM Lookup](actions/get-cnam-lookup.md) | `GET /lookup/cnam` | [docs](https://docs.seven.io/en/rest-api/endpoints/lookup#cnam) |
| [Get Contact](actions/get-contact.md) | `GET /contacts/:id` | [docs](https://docs.seven.io/en/rest-api/endpoints/contacts#retrieve-contact) |
| [Get Group](actions/get-group.md) | `GET /groups/:id` | [docs](https://docs.seven.io/en/rest-api/endpoints/groups#retrieve-a-group) |
| [Get HLR Lookup](actions/get-hlr-lookup.md) | `GET /lookup/hlr` | [docs](https://docs.seven.io/en/rest-api/endpoints/lookup#hlr) |
| [Get MNP Lookup](actions/get-mnp-lookup.md) | `GET /lookup/mnp` | [docs](https://docs.seven.io/en/rest-api/endpoints/lookup#mnp) |
| [Get Pricing](actions/get-pricing.md) | `GET /pricing` | [docs](https://docs.seven.io/en/rest-api/endpoints/account#prices) |
| [Get RCS Capabilities](actions/get-rcs-capabilities.md) | `GET /lookup/rcs` | [docs](https://docs.seven.io/en/rest-api/endpoints/lookup#rcs-capabilities) |
| [Get Statistics](actions/get-statistics.md) | `GET /analytics` | [docs](https://docs.seven.io/en/rest-api/endpoints/account#statistics) |
| [List Active Numbers](actions/list-active-numbers.md) | `GET /numbers/active` | [docs](https://docs.seven.io/en/rest-api/endpoints/numbers#active-numbers) |
| [List Available Numbers](actions/list-available-numbers.md) | `GET /numbers/available` | [docs](https://docs.seven.io/en/rest-api/endpoints/numbers#available-numbers) |
| [List Contacts](actions/list-contacts.md) | `GET /contacts` | [docs](https://docs.seven.io/en/rest-api/endpoints/contacts#query-contact-list) |
| [List Groups](actions/list-groups.md) | `GET /groups` | [docs](https://docs.seven.io/en/rest-api/endpoints/groups#list-all-groups) |
| [List Received SMS](actions/list-received-sms.md) | `GET /journal/inbound` | [docs](https://docs.seven.io/en/rest-api/endpoints/logbook#received-sms) |
| [List Sent Messages](actions/list-sent-messages.md) | `GET /journal/outbound` | [docs](https://docs.seven.io/en/rest-api/endpoints/logbook#sent-messages) |
| [List Subaccounts](actions/list-subaccounts.md) | `GET /subaccounts?action=read` | [docs](https://docs.seven.io/en/rest-api/endpoints/subaccounts#list-subaccounts) |
| [List Voice Messages](actions/list-voice-messages.md) | `GET /journal/voice` | [docs](https://docs.seven.io/en/rest-api/endpoints/logbook#voice-messages) |
| [List Webhooks](actions/list-webhooks.md) | `GET /hooks` | [docs](https://docs.seven.io/en/rest-api/endpoints/webhooks#show-active-webhooks) |
| [Order a Number](actions/order-a-number.md) | `POST /numbers/order` | [docs](https://docs.seven.io/en/rest-api/endpoints/numbers#order-a-number) |
| [Send SMS](actions/send-sms.md) | `POST /sms` | [docs](https://docs.seven.io/en/rest-api/endpoints/sms#send-sms) |
| [Send Voice Call](actions/send-voice-call.md) | `POST /voice` | [docs](https://docs.seven.io/en/rest-api/endpoints/voice#send-voice-call) |
| [Transfer Credits to Subaccount](actions/transfer-credits-to-subaccount.md) | `POST /subaccounts?action=transfer_credits` | [docs](https://docs.seven.io/en/rest-api/endpoints/subaccounts#manual-credit-transfer) |
| [Update Automatic Balance Transfer](actions/update-automatic-balance-transfer.md) | `POST /subaccounts?action=update` | [docs](https://docs.seven.io/en/rest-api/endpoints/subaccounts#automatic-balance-transfer) |
| [Update Contact](actions/update-contact.md) | `PATCH /contacts/:id` | [docs](https://docs.seven.io/en/rest-api/endpoints/contacts#update-contact) |
| [Update Group](actions/update-group.md) | `PATCH /groups/:id` | [docs](https://docs.seven.io/en/rest-api/endpoints/groups#update-a-group) |
| [Update Number](actions/update-number.md) | `PATCH /numbers/active/:number` | [docs](https://docs.seven.io/en/rest-api/endpoints/numbers#update-number) |
| [Validate Sender for Voice](actions/validate-sender-for-voice.md) | `POST /validate_for_voice` | [docs](https://docs.seven.io/en/rest-api/endpoints/sender-identifiers#validate-sender) |
