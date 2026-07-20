# Hook.Notifier: Native API Reference

A consolidated summary of Hook.Notifier's API configuration and 2 documented operations, with links to official documentation.

- **Official docs:** https://hooknotifier.com/blog/get-started-with-hook-notifier
- **API base URL:** `https://hooknotifier.com/{identifier}/{apiKey}`

## Authentication

### API Key

Use the Hook.Notifier identifier and key from your dashboard.

### Credentials

- **API Key:** `apiKey` · required
- **Identifier:** `identifier` · required · Your Hook.Notifier identifier from the dashboard.

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://hooknotifier.com/blog/get-started-with-hook-notifier)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Endpoints (2 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Send Notification](actions/send-notification.md) | `POST /` | [docs](https://hooknotifier.com/blog/get-started-with-hook-notifier) |
| [Verify Connection](actions/verify-connection.md) | `POST /` | [docs](https://hooknotifier.com/blog/get-started-with-hook-notifier) |
