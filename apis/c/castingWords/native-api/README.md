# CastingWords: Native API Reference

A consolidated summary of CastingWords's API configuration and 31 documented operations, with links to official documentation.

- **Official docs:** https://castingwords.com/docs/developer/SimpleAPI.html
- **API base URL:** `https://castingwords.com/store/API4`

## Authentication

### API Key

Authenticate with your CastingWords API key.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://castingwords.com/docs/developer/SimpleAPI.html)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Endpoints (31 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Add Extra Editing Upgrade](actions/add-extra-editing-upgrade.md) | `POST audiofile/:audiofile_id/upgrade` | [docs](https://castingwords.com/docs/developer/SimpleAPI.html#audiofileidupgrade) |
| [Add Timestamps Upgrade](actions/add-timestamps-upgrade.md) | `POST audiofile/:audiofile_id/upgrade` | [docs](https://castingwords.com/docs/developer/SimpleAPI.html#audiofileidupgrade) |
| [Create Test Transcript Order](actions/create-test-transcript-order.md) | `POST order_url` | [docs](https://castingwords.com/docs/developer/SimpleAPI.html#order_url) |
| [Get Prepay Balance](actions/get-prepay-balance.md) | `GET prepay_balance` | [docs](https://castingwords.com/docs/developer/SimpleAPI.html#prepay_balance) |
| [Get Webhook](actions/get-webhook.md) | `GET webhook` | [docs](https://castingwords.com/docs/developer/SimpleAPI.html#webhook) |
| [Order Budget Transcript](actions/order-budget-transcript.md) | `POST order_url` | [docs](https://castingwords.com/docs/developer/SimpleAPI.html#order_url) |
| [Order Budget Transcript Verbatim](actions/order-budget-transcript-verbatim.md) | `POST order_url` | [docs](https://castingwords.com/docs/developer/SimpleAPI.html#order_url) |
| [Order Budget Transcript With Captions](actions/order-budget-transcript-with-captions.md) | `POST order_url` | [docs](https://castingwords.com/docs/developer/SimpleAPI.html#order_url) |
| [Order Budget Transcript With Difficult Audio](actions/order-budget-transcript-with-difficult-audio.md) | `POST order_url` | [docs](https://castingwords.com/docs/developer/SimpleAPI.html#order_url) |
| [Order Budget Transcript With Timestamps](actions/order-budget-transcript-with-timestamps.md) | `POST order_url` | [docs](https://castingwords.com/docs/developer/SimpleAPI.html#order_url) |
| [Order Captions And Timestamps](actions/order-captions-and-timestamps.md) | `POST order_url` | [docs](https://castingwords.com/docs/developer/SimpleAPI.html#order_url) |
| [Order Difficult Audio With Timestamps](actions/order-difficult-audio-with-timestamps.md) | `POST order_url` | [docs](https://castingwords.com/docs/developer/SimpleAPI.html#order_url) |
| [Order Multiple Transcript URLs](actions/order-multiple-transcript-urls.md) | `POST order_url` | [docs](https://castingwords.com/docs/developer/SimpleAPI.html#order_url) |
| [Order Transcript With Notes](actions/order-transcript-with-notes.md) | `POST order_url` | [docs](https://castingwords.com/docs/developer/SimpleAPI.html#order_url) |
| [Order Transcript With Speaker Names](actions/order-transcript-with-speaker-names.md) | `POST order_url` | [docs](https://castingwords.com/docs/developer/SimpleAPI.html#order_url) |
| [Order Verbatim With Timestamps](actions/order-verbatim-with-timestamps.md) | `POST order_url` | [docs](https://castingwords.com/docs/developer/SimpleAPI.html#order_url) |
| [Order 1-Day Transcript](actions/order1-day-transcript.md) | `POST order_url` | [docs](https://castingwords.com/docs/developer/SimpleAPI.html#order_url) |
| [Order 1-Day Transcript With Captions](actions/order1-day-transcript-with-captions.md) | `POST order_url` | [docs](https://castingwords.com/docs/developer/SimpleAPI.html#order_url) |
| [Order 1-Day Transcript With Timestamps](actions/order1-day-transcript-with-timestamps.md) | `POST order_url` | [docs](https://castingwords.com/docs/developer/SimpleAPI.html#order_url) |
| [Order 7-Day Transcript](actions/order7-day-transcript.md) | `POST order_url` | [docs](https://castingwords.com/docs/developer/SimpleAPI.html#order_url) |
| [Order 7-Day Transcript With Captions](actions/order7-day-transcript-with-captions.md) | `POST order_url` | [docs](https://castingwords.com/docs/developer/SimpleAPI.html#order_url) |
| [Order 7-Day Transcript With Timestamps](actions/order7-day-transcript-with-timestamps.md) | `POST order_url` | [docs](https://castingwords.com/docs/developer/SimpleAPI.html#order_url) |
| [Refund Audiofile](actions/refund-audiofile.md) | `POST audiofile/:audiofile_id/refund` | [docs](https://castingwords.com/docs/developer/SimpleAPI.html#audiofileidrefund) |
| [Send Difficult Audio Webhook Test](actions/send-difficult-audio-webhook-test.md) | `POST webhook/test/DIFFICULT_AUDIO` | [docs](https://castingwords.com/docs/developer/SimpleAPI.html#receive-a-webhook-call) |
| [Send Refund Issued Webhook Test](actions/send-refund-issued-webhook-test.md) | `POST webhook/test/REFUND_ISSUED` | [docs](https://castingwords.com/docs/developer/SimpleAPI.html#receive-a-webhook-call) |
| [Send Transcript Complete Webhook Test](actions/send-transcript-complete-webhook-test.md) | `POST webhook/test/TRANSCRIPT_COMPLETE` | [docs](https://castingwords.com/docs/developer/SimpleAPI.html#receive-a-webhook-call) |
| [Set Webhook](actions/set-webhook.md) | `POST webhook` | [docs](https://castingwords.com/docs/developer/SimpleAPI.html#webhook) |
| [Upgrade Budget To 1-Day](actions/upgrade-budget-to1-day.md) | `POST audiofile/:audiofile_id/upgrade` | [docs](https://castingwords.com/docs/developer/SimpleAPI.html#audiofileidupgrade) |
| [Upgrade Budget To 7-Day](actions/upgrade-budget-to7-day.md) | `POST audiofile/:audiofile_id/upgrade` | [docs](https://castingwords.com/docs/developer/SimpleAPI.html#audiofileidupgrade) |
| [Upgrade To Difficult Audio](actions/upgrade-to-difficult-audio.md) | `POST audiofile/:audiofile_id/upgrade` | [docs](https://castingwords.com/docs/developer/SimpleAPI.html#audiofileidupgrade) |
| [Upgrade 7-Day To 1-Day](actions/upgrade7-day-to1-day.md) | `POST audiofile/:audiofile_id/upgrade` | [docs](https://castingwords.com/docs/developer/SimpleAPI.html#audiofileidupgrade) |
