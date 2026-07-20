# ExpertTexting: Native API Reference

A consolidated summary of ExpertTexting's API configuration and 6 documented operations, with links to official documentation.

- **Official docs:** https://www.experttexting.com/appv2/documentation/index/
- **API base URL:** `https://www.experttexting.com`

## Authentication

### API Key

Connect with your ExpertTexting username, API key, and API secret from Account Settings.

### Credentials

- **API Key:** `apiKey` · required
- **Username:** `username` · required · Your ExpertTexting account username from Account Settings.
- **API Secret:** `apiSecret` · required · Your ExpertTexting API Secret from Account Settings.

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://www.experttexting.com/appv2/documentation/index/)

## Endpoints (6 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Check Balance](actions/check-balance.md) | `GET /ExptRestApi/sms/json/Account/Balance` | [docs](https://www.experttexting.com/appv2/Documentation/Balance) |
| [Check Message Status](actions/check-message-status.md) | `GET /ExptRestApi/sms/json/Message/Status` | [docs](https://www.experttexting.com/appv2/Documentation/Status) |
| [List Unread Inbox Messages](actions/list-unread-inbox-messages.md) | `GET /ExptRestApi/sms/json/Message/UnreadInbox` | [docs](https://www.experttexting.com/appv2/Documentation/UnreadInbox) |
| [Send MMS](actions/send-mms.md) | `POST /ExptRestAPI/json/mms/send` | [docs](https://www.experttexting.com/appv2/Documentation/SendMMS) |
| [Send SMS](actions/send-sms.md) | `POST /ExptRestApi/sms/json/Message/Send` | [docs](https://www.experttexting.com/appv2/Documentation/Send) |
| [Send Unicode SMS](actions/send-unicode-sms.md) | `POST /ExptRestApi/sms/json/Message/Send` | [docs](https://www.experttexting.com/appv2/Documentation/Send) |
