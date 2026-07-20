# Webpushr: Native API Reference

A consolidated summary of Webpushr's API configuration and 6 documented operations, with links to official documentation.

- **Official docs:** https://www.webpushr.com/docs/introduction-to-rest-api
- **API base URL:** `https://api.webpushr.com/v1`

## Authentication

### Header Credentials

Use your site-specific Webpushr REST API key and authentication token headers.

### Credentials

- **API Key:** `apiKey` · required · Site-specific Webpushr REST API key from Integration > API Keys. Stored as a credential field and interpolated into the request header.
- **Authentication Token:** `authToken` · required · Site-specific Webpushr authentication token from Integration > API Keys. Stored as a credential field and interpolated into the request header.

Send these headers with each API request:

```http
webpushrKey: <apiKey>
webpushrAuthToken: <webpushrAuthToken>
```

[Official authentication documentation](https://www.webpushr.com/docs/authenticating-api-calls)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Endpoints (6 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Get Push Status](actions/get-push-status.md) | `GET /notification/status/id/:campaignId` | [docs](https://www.webpushr.com/docs/check-push-notification-status) |
| [Get Subscriber Count](actions/get-subscriber-count.md) | `GET /site/subscriber_count` | [docs](https://www.webpushr.com/docs/check-subscriber-count) |
| [Send Push to All Subscribers](actions/send-push-to-all-subscribers.md) | `POST /notification/send/all` | [docs](https://www.webpushr.com/docs/send-push-to-all-subscribers) |
| [Send Push to Custom Attributes](actions/send-push-to-custom-attributes.md) | `POST /notification/send/attribute` | [docs](https://www.webpushr.com/docs/send-push-to-a-custom-attribute) |
| [Send Push to Segments](actions/send-push-to-segments.md) | `POST /notification/send/segment` | [docs](https://www.webpushr.com/docs/send-push-to-a-segment) |
| [Send Push to Subscriber ID](actions/send-push-to-subscriber-id.md) | `POST /notification/send/sid` | [docs](https://www.webpushr.com/docs/send-push-to-a-subscriber-id) |
