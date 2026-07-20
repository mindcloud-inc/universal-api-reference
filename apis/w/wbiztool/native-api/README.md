# Wbiztool: Native API Reference

A consolidated summary of Wbiztool's API configuration and 23 documented operations, with links to official documentation.

- **Official docs:** https://wbiztool.com/docs/
- **API base URL:** `https://wbiztool.com/api/v1`

## Authentication

### API Key

Use your Wbiztool client ID, API key, and WhatsApp client ID.

### Credentials

- **API Key:** `apiKey` · required
- **WhatsApp Client ID:** `whatsappClient` · required · Your connected WhatsApp client ID from the WhatsApp Settings page.
- **Client ID:** `clientId` · required · Your Wbiztool client ID from the API Keys page.

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://wbiztool.com/docs/check-my-creds-api/)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Endpoints (23 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Cancel Message](actions/cancel-message.md) | `POST /cancel_msg/` | [docs](https://wbiztool.com/docs/cancel-message-api/) |
| [Check Credentials](actions/check-credentials.md) | `POST /me/` | [docs](https://wbiztool.com/docs/check-my-creds-api/) |
| [Connect WhatsApp Number](actions/connect-whats-app-number.md) | `POST /whatsapp/connect/` | [docs](https://wbiztool.com/docs/whatsapp-connect-api/) |
| [Create Reminder](actions/create-reminder.md) | `POST /reminder/create/` | [docs](https://wbiztool.com/docs/reminder-create-api/) |
| [Create Verification Campaign](actions/create-verification-campaign.md) | `POST /verification/create/` | [docs](https://wbiztool.com/docs/verification-create-api/) |
| [Get Current WhatsApp Client Status](actions/get-current-whats-app-client-status.md) | `POST /whatsapp-client/status/` | [docs](https://wbiztool.com/docs/whatsapp-client-status-api/) |
| [Get Media File](actions/get-media-file.md) | `POST /media/{{media_id}}/` | [docs](https://wbiztool.com/docs/media-get-api/) |
| [Get Message Status](actions/get-message-status.md) | `POST /message/status/{{message_id}}/` | [docs](https://wbiztool.com/docs/message-status-api/) |
| [Get Verification Status](actions/get-verification-status.md) | `GET /verification/status/` | [docs](https://wbiztool.com/docs/verification-status-api/) |
| [Get WhatsApp Client Status By Id](actions/get-whats-app-client-status-by-id.md) | `POST /whatsapp/status/{{whatsapp_client_id}}/` | [docs](https://wbiztool.com/docs/whatsapp-client-status-by-id-api/) |
| [List Media Files](actions/list-media-files.md) | `POST /media/list/` | [docs](https://wbiztool.com/docs/media-list-api/) |
| [List Message History](actions/list-message-history.md) | `POST /report/` | [docs](https://wbiztool.com/docs/history-messages-api/) |
| [List Reminders](actions/list-reminders.md) | `POST /reminder/list/` | [docs](https://wbiztool.com/docs/reminder-list-api/) |
| [List Verification Results](actions/list-verification-results.md) | `GET /verification/results/` | [docs](https://wbiztool.com/docs/verification-results-api/) |
| [List WhatsApp Accounts](actions/list-whats-app-accounts.md) | `POST /whatsapp/accounts/` | [docs](https://wbiztool.com/docs/whatsapp-accounts-api/) |
| [Schedule File Message](actions/schedule-file-message.md) | `POST /schedule_msg/` | [docs](https://wbiztool.com/docs/schedule-message-api/) |
| [Schedule Image Message](actions/schedule-image-message.md) | `POST /schedule_msg/` | [docs](https://wbiztool.com/docs/schedule-message-api/) |
| [Schedule Text Message](actions/schedule-text-message.md) | `POST /schedule_msg/` | [docs](https://wbiztool.com/docs/schedule-message-api/) |
| [Send File Message](actions/send-file-message.md) | `POST /send_msg/` | [docs](https://wbiztool.com/docs/send-message-api/) |
| [Send Image Message](actions/send-image-message.md) | `POST /send_msg/` | [docs](https://wbiztool.com/docs/send-message-api/) |
| [Send Multi Messages](actions/send-multi-messages.md) | `POST /send_msg/multi/` | [docs](https://wbiztool.com/docs/send-msg-multi-api/) |
| [Send Text Message](actions/send-text-message.md) | `POST /send_msg/` | [docs](https://wbiztool.com/docs/send-message-api/) |
| [Upload Media](actions/upload-media.md) | `POST /media/upload/` | [docs](https://wbiztool.com/docs/media-upload-api/) |
