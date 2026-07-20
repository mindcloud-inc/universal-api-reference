# Morf: Native API Reference

A consolidated summary of Morf's API configuration and 1 documented operations, with links to official documentation.

- **Official docs:** https://www.morf.health/docs/events/payloads/morf/track
- **API base URL:** `{trackWebhookUrl}`

## Authentication

### Morf Track Webhook

Connect Morf using a Track workflow webhook URL and source_id write key.

### Credentials

- **Track Webhook URL:** `trackWebhookUrl` · required · Full Morf Track webhook URL from the workflow trigger Connect tab.
- **Track Write Key:** `trackWriteKey` · required · The source_id write key for the Morf Track workflow.

[Official authentication documentation](https://www.morf.health/docs/events/payloads/morf/track)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Endpoints (1 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Send Track Event](actions/send-track-event.md) | `POST` | [docs](https://www.morf.health/docs/events/payloads/morf/track) |
