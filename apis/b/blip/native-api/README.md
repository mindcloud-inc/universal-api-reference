# Blip: Native API Reference

A consolidated summary of Blip's API configuration and 40 documented operations, with links to official documentation.

- **Official docs:** https://docs.blip.ai/
- **API base URL:** `https://ae2bd556-b116-4f7a-a0d3-30a54ef5b9d7.http.msging.net`

## Authentication

### Authorization Header

Use the exact BLiP HTTP authorization header value from the bot connection settings.

### Credentials

- **Authorization Header:** `authorization` · required · Paste the full BLiP HTTP Authorization header value exactly as shown in the BLiP portal, including the `Key ` prefix.

Send these headers with each API request:

```http
Authorization: <authorization>
```

[Official authentication documentation](https://docs.blip.ai/#authentication)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Endpoints (40 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Add Contact](actions/add-contact.md) | `POST /commands` | [docs](https://docs.blip.ai/#add-a-contact) |
| [Associate Answer to Intent](actions/associate-answer-to-intent.md) | `POST /commands` | [docs](https://docs.blip.ai/#associate-answers-to-an-intent) |
| [Associate Question to Intent](actions/associate-question-to-intent.md) | `POST /commands` | [docs](https://docs.blip.ai/#associate-questions-to-an-intent) |
| [Cancel Scheduling](actions/cancel-scheduling.md) | `POST /commands` | [docs](https://docs.blip.ai/#cancel-a-scheduling) |
| [Create Distribution List](actions/create-distribution-list.md) | `POST /commands` | [docs](https://docs.blip.ai/#create-a-list) |
| [Create Entity](actions/create-entity.md) | `POST /commands` | [docs](https://docs.blip.ai/#create-an-entity) |
| [Create Intent](actions/create-intent.md) | `POST /commands` | [docs](https://docs.blip.ai/#intention) |
| [Create Scheduling](actions/create-scheduling.md) | `POST /commands` | [docs](https://docs.blip.ai/#create-a-scheduling) |
| [Delete Answer from Intent](actions/delete-answer-from-intent.md) | `POST /commands` | [docs](https://docs.blip.ai/#delete-answer-from-intent) |
| [Delete Contact](actions/delete-contact.md) | `POST /commands` | [docs](https://docs.blip.ai/#contacts) |
| [Delete Distribution List](actions/delete-distribution-list.md) | `POST /commands` | [docs](https://docs.blip.ai/#delete-a-list) |
| [Delete Document](actions/delete-document.md) | `POST /commands` | [docs](https://docs.blip.ai/#delete-a-document) |
| [Delete Question from Intent](actions/delete-question-from-intent.md) | `POST /commands` | [docs](https://docs.blip.ai/#delete-question-from-intent) |
| [Get Account](actions/get-account.md) | `POST /commands` | [docs](https://docs.blip.ai/#account) |
| [Get Call Dashboard Detail](actions/get-call-dashboard-detail.md) | `POST /commands` | [docs](https://docs.blip.ai/#get-call-dashboard-detail) |
| [Get Call Dashboard Summary](actions/get-call-dashboard-summary.md) | `POST /commands` | [docs](https://docs.blip.ai/#get-call-dashboard-summary) |
| [Get Call Reject Reasons](actions/get-call-reject-reasons.md) | `POST /commands` | [docs](https://docs.blip.ai/#get-call-reject-reasons) |
| [Get Contact](actions/get-contact.md) | `POST /commands` | [docs](https://docs.blip.ai/#get-contact) |
| [Get Document](actions/get-document.md) | `POST /commands` | [docs](https://docs.blip.ai/#get-a-document) |
| [Get Entity](actions/get-entity.md) | `POST /commands` | [docs](https://docs.blip.ai/#get-an-entity) |
| [Get Intent](actions/get-intent.md) | `POST /commands` | [docs](https://docs.blip.ai/#intention) |
| [Get Scheduled Message](actions/get-scheduled-message.md) | `POST /commands` | [docs](https://docs.blip.ai/#get-a-scheduled-message) |
| [List Analysis](actions/list-analysis.md) | `POST /commands` | [docs](https://docs.blip.ai/#get-the-last-10-analysis) |
| [List Attendants](actions/list-attendants.md) | `POST /commands` | [docs](https://docs.blip.ai/#attendant) |
| [List Closed Tickets](actions/list-closed-tickets.md) | `POST /commands` | [docs](https://docs.blip.ai/#get-all-closed-tickets) |
| [List Contacts](actions/list-contacts.md) | `POST /commands` | [docs](https://docs.blip.ai/#get-contacts) |
| [List Distribution Lists](actions/list-distribution-lists.md) | `POST /commands` | [docs](https://docs.blip.ai/#get-all-lists) |
| [List Documents](actions/list-documents.md) | `POST /commands` | [docs](https://docs.blip.ai/#get-a-document-collection) |
| [List Entities](actions/list-entities.md) | `POST /commands` | [docs](https://docs.blip.ai/#entity) |
| [List Intent Answers](actions/list-intent-answers.md) | `POST /commands` | [docs](https://docs.blip.ai/#get-answers-from-an-intent) |
| [List Intent Questions](actions/list-intent-questions.md) | `POST /commands` | [docs](https://docs.blip.ai/#get-questions-from-an-intent) |
| [List Intents](actions/list-intents.md) | `POST /commands` | [docs](https://docs.blip.ai/#intention) |
| [List Last Messages](actions/list-last-messages.md) | `POST /commands` | [docs](https://docs.blip.ai/#get-last-messages) |
| [List Logged Messages](actions/list-logged-messages.md) | `POST /commands` | [docs](https://docs.blip.ai/#get-logged-messages) |
| [List Open Tickets](actions/list-open-tickets.md) | `POST /commands` | [docs](https://docs.blip.ai/#get-all-active-tickets) |
| [List Schedules](actions/list-schedules.md) | `POST /commands` | [docs](https://docs.blip.ai/#get-all-schedules) |
| [List Tickets](actions/list-tickets.md) | `POST /commands` | [docs](https://docs.blip.ai/#get-all-tickets-of-a-bot) |
| [Ping](actions/ping.md) | `POST /commands` | [docs](https://docs.blip.ai/#authentication) |
| [Store Custom Document](actions/store-custom-document.md) | `POST /commands` | [docs](https://docs.blip.ai/#bucket) |
| [Toggle Message and Notification Logs](actions/toggle-message-and-notification-logs.md) | `POST /commands` | [docs](https://docs.blip.ai/#toggle-message-and-notification-logs) |
