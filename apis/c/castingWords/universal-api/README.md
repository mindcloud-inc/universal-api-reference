# <img src="https://images.mindcloud.co/apps/icons/casting-words_1776255833246.png" alt="CastingWords logo" width="28" height="28"> CastingWords: Universal API

Order transcripts, track audiofiles, download transcripts, and manage webhooks

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/castingWords/latest
- **Category:** Business Intelligence / Data Extraction
- **Actions:** 31
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://castingwords.com
- **Vendor API docs:** https://castingwords.com/docs/developer/SimpleAPI.html

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Prepay Balance](actions/get-prepay-balance.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/castingWords/latest/actions/get-prepay-balance?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (31)

### Audiofile

| Action | Method | Description |
| --- | --- | --- |
| [Add Extra Editing Upgrade](actions/add-extra-editing-upgrade.md) | PUT | Updates a CastingWords order to add extra editing. |
| [Add Timestamps Upgrade](actions/add-timestamps-upgrade.md) | PUT | Updates a CastingWords order to add timestamps. |
| [Refund Audiofile](actions/refund-audiofile.md) | PUT | Updates a CastingWords audiofile by issuing a refund. |
| [Upgrade Budget To 1-Day](actions/upgrade-budget-to1-day.md) | PUT | Updates a budget CastingWords order to 1-day service. |
| [Upgrade Budget To 7-Day](actions/upgrade-budget-to7-day.md) | PUT | Updates a budget CastingWords order to 7-day service. |
| [Upgrade To Difficult Audio](actions/upgrade-to-difficult-audio.md) | PUT | Updates a CastingWords order to difficult audio. |
| [Upgrade 7-Day To 1-Day](actions/upgrade7-day-to1-day.md) | PUT | Updates a 7-day CastingWords order to 1-day service. |

### Order

| Action | Method | Description |
| --- | --- | --- |
| [Create Test Transcript Order](actions/create-test-transcript-order.md) | POST | Creates a test transcript order in CastingWords. |
| [Order Budget Transcript](actions/order-budget-transcript.md) | POST | Creates a budget transcript order in CastingWords. |
| [Order Budget Transcript Verbatim](actions/order-budget-transcript-verbatim.md) | POST | Creates a budget verbatim transcript order in CastingWords. |
| [Order Budget Transcript With Captions](actions/order-budget-transcript-with-captions.md) | POST | Creates a budget transcript order with captions in CastingWords. |
| [Order Budget Transcript With Difficult Audio](actions/order-budget-transcript-with-difficult-audio.md) | POST | Creates a budget transcript order for difficult audio in CastingWords. |
| [Order Budget Transcript With Timestamps](actions/order-budget-transcript-with-timestamps.md) | POST | Creates a budget transcript order with timestamps in CastingWords. |
| [Order Captions And Timestamps](actions/order-captions-and-timestamps.md) | POST | Creates a transcript order with captions and timestamps in CastingWords. |
| [Order Difficult Audio With Timestamps](actions/order-difficult-audio-with-timestamps.md) | POST | Creates a difficult-audio transcript order with timestamps in CastingWords. |
| [Order Multiple Transcript URLs](actions/order-multiple-transcript-urls.md) | POST | Creates transcript orders from multiple URLs in CastingWords. |
| [Order Transcript With Notes](actions/order-transcript-with-notes.md) | POST | Creates a transcript order with notes in CastingWords. |
| [Order Transcript With Speaker Names](actions/order-transcript-with-speaker-names.md) | POST | Creates a transcript order with speaker names in CastingWords. |
| [Order Verbatim With Timestamps](actions/order-verbatim-with-timestamps.md) | POST | Creates a verbatim transcript order with timestamps in CastingWords. |
| [Order 1-Day Transcript](actions/order1-day-transcript.md) | POST | Creates a 1-day transcript order in CastingWords. |
| [Order 1-Day Transcript With Captions](actions/order1-day-transcript-with-captions.md) | POST | Creates a 1-day transcript order with captions in CastingWords. |
| [Order 1-Day Transcript With Timestamps](actions/order1-day-transcript-with-timestamps.md) | POST | Creates a 1-day transcript order with timestamps in CastingWords. |
| [Order 7-Day Transcript](actions/order7-day-transcript.md) | POST | Creates a 7-day transcript order in CastingWords. |
| [Order 7-Day Transcript With Captions](actions/order7-day-transcript-with-captions.md) | POST | Creates a 7-day transcript order with captions in CastingWords. |
| [Order 7-Day Transcript With Timestamps](actions/order7-day-transcript-with-timestamps.md) | POST | Creates a 7-day transcript order with timestamps in CastingWords. |

### Prepay Balance

| Action | Method | Description |
| --- | --- | --- |
| [Get Prepay Balance](actions/get-prepay-balance.md) | GET | Retrieves prepay balance from CastingWords. |

### Webhook

| Action | Method | Description |
| --- | --- | --- |
| [Get Webhook](actions/get-webhook.md) | GET | Retrieves webhook settings from CastingWords. |
| [Set Webhook](actions/set-webhook.md) | PUT | Updates webhook settings in CastingWords. |

### Webhook Test

| Action | Method | Description |
| --- | --- | --- |
| [Send Difficult Audio Webhook Test](actions/send-difficult-audio-webhook-test.md) | POST | Sends a difficult audio webhook test from CastingWords. |
| [Send Refund Issued Webhook Test](actions/send-refund-issued-webhook-test.md) | POST | Sends a refund issued webhook test from CastingWords. |
| [Send Transcript Complete Webhook Test](actions/send-transcript-complete-webhook-test.md) | POST | Sends a transcript complete webhook test from CastingWords. |

