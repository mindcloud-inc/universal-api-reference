# SyncMate: Native API Reference

A consolidated summary of SyncMate's API configuration and 10 documented operations, with links to official documentation.

- **Official docs:** https://assistro.co/user-guide/developer-guide/connect-your-custom-app-with-syncmate/
- **API base URL:** `https://app.assistro.co`

## Authentication

### API Key

Use your SyncMate bearer API key from the Assistro dashboard.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://assistro.co/user-guide/developer-guide/syncmate-user-guide-regenerating-your-token/)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Endpoints (10 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Check Connection](actions/check-connection.md) | `POST /api/wapushplus/checkconnection` | [docs](https://www.postman.com/syncmate/request/52527883-c1bef907-60a4-4245-a82f-5927bfb5c435) |
| [Check WhatsApp Number](actions/check-whats-app-number.md) | `POST /api/wapushplus/checkconnection` | [docs](https://www.postman.com/syncmate/request/52527883-97b781a8-62ed-4fe9-83bc-cc18e04d607c) |
| [Connect WhatsApp Session](actions/connect-whats-app-session.md) | `POST /api/wapushplus/getqr` | [docs](https://www.postman.com/syncmate/request/52527883-50722693-5150-4448-bef1-8e19a4f9bf0c) |
| [Disconnect WhatsApp Session](actions/disconnect-whats-app-session.md) | `POST /api/wapushplus/disconnect` | [docs](https://www.postman.com/syncmate/request/52527883-385ca313-d8fa-4d5b-a045-92b2353acc5d) |
| [Get Group Participants](actions/get-group-participants.md) | `GET /api/group/:groupId` | [docs](https://www.postman.com/syncmate/request/52527883-339e4251-8202-44a9-9435-4ee8112eeb7f) |
| [Get Groups](actions/get-groups.md) | `GET /api/groups` | [docs](https://www.postman.com/syncmate/request/52527883-a75e7405-47c3-423f-87b4-5452bd0d5973) |
| [Send Bulk Message](actions/send-bulk-message.md) | `POST /api/v1/wapushplus/bulk/message` | [docs](https://assistro.co/user-guide/developer-guide/connect-your-custom-app-with-syncmate/) |
| [Send Message To A Channel/Newsletter Via SyncMate](actions/send-message-to-a-channel-newsletter-via-sync-mate.md) | `POST /api/v1/wapushplus/single/message` | [docs](https://assistro.co/user-guide/zapier/how-to-send-a-whatsapp-notification-to-any-group-or-channel/) |
| [Send Single Message](actions/send-single-message.md) | `POST /api/v1/wapushplus/single/message` | [docs](https://assistro.co/user-guide/developer-guide/connect-your-custom-app-with-syncmate/) |
| [Send WhatsApp Group Message Via SyncMate](actions/send-whats-app-group-message-via-sync-mate.md) | `POST /api/v1/wapushplus/single/message` | [docs](https://assistro.co/user-guide/zapier/how-to-send-a-whatsapp-notification-to-any-group-or-channel/) |
