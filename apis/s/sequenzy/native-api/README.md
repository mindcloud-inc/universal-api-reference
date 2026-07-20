# Sequenzy: Native API Reference

A consolidated summary of Sequenzy's API configuration and 28 documented operations, with links to official documentation.

- **Official docs:** https://docs.sequenzy.com/api-reference/introduction
- **API base URL:** `https://api.sequenzy.com/api/v1`

## Authentication

### API Key

Use your Sequenzy API key from the Sequenzy dashboard. The runtime sends it as a bearer token in the Authorization header.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://docs.sequenzy.com/api-reference/introduction)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Endpoints (28 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Add Tag](actions/add-tag.md) | `POST /subscribers/tags` | [docs](https://docs.sequenzy.com/api-reference/subscribers/tags/add) |
| [Add Tags (Bulk)](actions/add-tags-bulk.md) | `POST /subscribers/tags/bulk` | [docs](https://docs.sequenzy.com/api-reference/subscribers/tags/add-bulk) |
| [Create Sequence with AI](actions/create-sequence-with-ai.md) | `POST /sequences` | [docs](https://docs.sequenzy.com/api-reference/sequences/create) |
| [Create Sequence with Steps](actions/create-sequence-with-steps.md) | `POST /sequences` | [docs](https://docs.sequenzy.com/api-reference/sequences/create) |
| [Create Subscriber](actions/create-subscriber.md) | `POST /subscribers` | [docs](https://docs.sequenzy.com/api-reference/subscribers/create) |
| [Create Subscriber Without Lists](actions/create-subscriber-without-lists.md) | `POST /subscribers` | [docs](https://docs.sequenzy.com/api-reference/subscribers/create) |
| [Create Subscriber Without Sequence Enrollment](actions/create-subscriber-without-sequence-enrollment.md) | `POST /subscribers` | [docs](https://docs.sequenzy.com/api-reference/subscribers/create) |
| [Create Unsubscribed Subscriber](actions/create-unsubscribed-subscriber.md) | `POST /subscribers` | [docs](https://docs.sequenzy.com/api-reference/subscribers/create) |
| [Delete Subscriber](actions/delete-subscriber.md) | `DELETE /subscribers/:email` | [docs](https://docs.sequenzy.com/api-reference/subscribers/delete) |
| [Get Account Metrics](actions/get-account-metrics.md) | `GET /metrics` | [docs](https://docs.sequenzy.com/api-reference/analytics/metrics) |
| [Get Account Metrics (Custom Range)](actions/get-account-metrics-custom-range.md) | `GET /metrics` | [docs](https://docs.sequenzy.com/api-reference/analytics/metrics) |
| [Get Account Metrics (24h)](actions/get-account-metrics24h.md) | `GET /metrics` | [docs](https://docs.sequenzy.com/api-reference/analytics/metrics) |
| [Get Account Metrics (30d)](actions/get-account-metrics30d.md) | `GET /metrics` | [docs](https://docs.sequenzy.com/api-reference/analytics/metrics) |
| [Get Preferences Token](actions/get-preferences-token.md) | `POST /widgets/preferences/token` | [docs](https://docs.sequenzy.com/api-reference/widgets/preferences-token) |
| [Get Recipient Metrics](actions/get-recipient-metrics.md) | `GET /metrics/recipients` | [docs](https://docs.sequenzy.com/api-reference/analytics/recipients) |
| [Get Recipient Metrics by Email](actions/get-recipient-metrics-by-email.md) | `GET /metrics/recipients` | [docs](https://docs.sequenzy.com/api-reference/analytics/recipients) |
| [Get Recipient Metrics by Sequence](actions/get-recipient-metrics-by-sequence.md) | `GET /metrics/recipients` | [docs](https://docs.sequenzy.com/api-reference/analytics/recipients) |
| [Get Recipient Metrics (30d)](actions/get-recipient-metrics30d.md) | `GET /metrics/recipients` | [docs](https://docs.sequenzy.com/api-reference/analytics/recipients) |
| [Get Sequence](actions/get-sequence.md) | `GET /sequences/:sequenceId` | [docs](https://docs.sequenzy.com/api-reference/sequences/create) |
| [Get Subscriber](actions/get-subscriber.md) | `GET /subscribers/:email` | [docs](https://docs.sequenzy.com/api-reference/subscribers/get) |
| [List Subscribers](actions/list-subscribers.md) | `GET /subscribers` | [docs](https://docs.sequenzy.com/api-reference/subscribers/list) |
| [List Transactional Emails](actions/list-transactional-emails.md) | `GET /transactional` | [docs](https://docs.sequenzy.com/api-reference/transactional/list) |
| [Merge Subscriber](actions/merge-subscriber.md) | `POST /subscribers` | [docs](https://docs.sequenzy.com/api-reference/subscribers/create) |
| [Overwrite Subscriber](actions/overwrite-subscriber.md) | `POST /subscribers` | [docs](https://docs.sequenzy.com/api-reference/subscribers/create) |
| [Trigger Event](actions/trigger-event.md) | `POST /subscribers/events` | [docs](https://docs.sequenzy.com/api-reference/subscribers/events/trigger) |
| [Trigger Events (Bulk)](actions/trigger-events-bulk.md) | `POST /subscribers/events/bulk` | [docs](https://docs.sequenzy.com/api-reference/subscribers/events/trigger-bulk) |
| [Unsubscribe Subscriber](actions/unsubscribe-subscriber.md) | `PATCH /subscribers/:email` | [docs](https://docs.sequenzy.com/api-reference/subscribers/update) |
| [Update Subscriber](actions/update-subscriber.md) | `PATCH /subscribers/:email` | [docs](https://docs.sequenzy.com/api-reference/subscribers/update) |
