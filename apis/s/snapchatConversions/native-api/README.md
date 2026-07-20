# Snapchat Conversions: Native API Reference

A consolidated summary of Snapchat Conversions's API configuration and 40 documented operations, with links to official documentation.

- **Official docs:** https://developers.snap.com/api/marketing-api/Conversions-API/Introduction
- **API base URL:** `https://adsapi.snapchat.com/v1`

## Authentication

### API Token

Use a long-lived Snapchat Conversions API token from Business Details.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://developers.snap.com/api/marketing-api/Ads-API/signal-readiness-api)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON. Response data is read from `event_quality_scores`.

## Endpoints (40 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Get App Signal Readiness Scores](actions/get-app-signal-readiness-scores.md) | `GET /mobile_apps/:snapAppId/event_quality_scores` | [docs](https://developers.snap.com/api/marketing-api/Ads-API/signal-readiness-api) |
| [Get Pixel Signal Readiness Scores](actions/get-pixel-signal-readiness-scores.md) | `GET /pixels/:pixelId/event_quality_scores` | [docs](https://developers.snap.com/api/marketing-api/Ads-API/signal-readiness-api) |
| [Get Test Event Logs](actions/get-test-event-logs.md) | `GET https://tr.snapchat.com/v3/:asset_id/events/validate/logs` | [docs](https://developers.snap.com/api/marketing-api/Conversions-API/VerifySetUp) |
| [Get Test Event Stats](actions/get-test-event-stats.md) | `GET https://tr.snapchat.com/v3/:asset_id/events/validate/stats` | [docs](https://developers.snap.com/api/marketing-api/Conversions-API/VerifySetUp) |
| [Send Achievement Unlocked Event](actions/send-achievement-unlocked-event.md) | `POST https://tr.snapchat.com/v3/:asset_id/events` | [docs](https://developers.snap.com/api/marketing-api/Conversions-API/Parameters) |
| [Send Ad Click Event](actions/send-ad-click-event.md) | `POST https://tr.snapchat.com/v3/:asset_id/events` | [docs](https://developers.snap.com/api/marketing-api/Conversions-API/Parameters) |
| [Send Ad View Event](actions/send-ad-view-event.md) | `POST https://tr.snapchat.com/v3/:asset_id/events` | [docs](https://developers.snap.com/api/marketing-api/Conversions-API/Parameters) |
| [Send Add Billing Event](actions/send-add-billing-event.md) | `POST https://tr.snapchat.com/v3/:asset_id/events` | [docs](https://developers.snap.com/api/marketing-api/Conversions-API/Parameters) |
| [Send Add Cart Event](actions/send-add-cart-event.md) | `POST https://tr.snapchat.com/v3/:asset_id/events` | [docs](https://developers.snap.com/api/marketing-api/Conversions-API/Parameters) |
| [Send Add To Wishlist Event](actions/send-add-to-wishlist-event.md) | `POST https://tr.snapchat.com/v3/:asset_id/events` | [docs](https://developers.snap.com/api/marketing-api/Conversions-API/Parameters) |
| [Send App Batch Events](actions/send-app-batch-events.md) | `POST https://tr.snapchat.com/v3/:snap_app_id/events` | [docs](https://developers.snap.com/api/marketing-api/Conversions-API/UsingTheAPI) |
| [Send App Install Event](actions/send-app-install-event.md) | `POST https://tr.snapchat.com/v3/:asset_id/events` | [docs](https://developers.snap.com/api/marketing-api/Conversions-API/Parameters) |
| [Send App Open Event](actions/send-app-open-event.md) | `POST https://tr.snapchat.com/v3/:asset_id/events` | [docs](https://developers.snap.com/api/marketing-api/Conversions-API/Parameters) |
| [Send Complete Tutorial Event](actions/send-complete-tutorial-event.md) | `POST https://tr.snapchat.com/v3/:asset_id/events` | [docs](https://developers.snap.com/api/marketing-api/Conversions-API/Parameters) |
| [Send Custom Event 1](actions/send-custom-event1.md) | `POST https://tr.snapchat.com/v3/:asset_id/events` | [docs](https://developers.snap.com/api/marketing-api/Conversions-API/Parameters) |
| [Send Custom Event 2](actions/send-custom-event2.md) | `POST https://tr.snapchat.com/v3/:asset_id/events` | [docs](https://developers.snap.com/api/marketing-api/Conversions-API/Parameters) |
| [Send Custom Event 3](actions/send-custom-event3.md) | `POST https://tr.snapchat.com/v3/:asset_id/events` | [docs](https://developers.snap.com/api/marketing-api/Conversions-API/Parameters) |
| [Send Custom Event 4](actions/send-custom-event4.md) | `POST https://tr.snapchat.com/v3/:asset_id/events` | [docs](https://developers.snap.com/api/marketing-api/Conversions-API/Parameters) |
| [Send Custom Event 5](actions/send-custom-event5.md) | `POST https://tr.snapchat.com/v3/:asset_id/events` | [docs](https://developers.snap.com/api/marketing-api/Conversions-API/Parameters) |
| [Send Invite Event](actions/send-invite-event.md) | `POST https://tr.snapchat.com/v3/:asset_id/events` | [docs](https://developers.snap.com/api/marketing-api/Conversions-API/Parameters) |
| [Send Level Complete Event](actions/send-level-complete-event.md) | `POST https://tr.snapchat.com/v3/:asset_id/events` | [docs](https://developers.snap.com/api/marketing-api/Conversions-API/Parameters) |
| [Send List View Event](actions/send-list-view-event.md) | `POST https://tr.snapchat.com/v3/:asset_id/events` | [docs](https://developers.snap.com/api/marketing-api/Conversions-API/Parameters) |
| [Send Login Event](actions/send-login-event.md) | `POST https://tr.snapchat.com/v3/:asset_id/events` | [docs](https://developers.snap.com/api/marketing-api/Conversions-API/Parameters) |
| [Send Mixed Event Batch](actions/send-mixed-event-batch.md) | `POST https://tr.snapchat.com/v3/:asset_id/events` | [docs](https://developers.snap.com/api/marketing-api/Conversions-API/UsingTheAPI) |
| [Send Offline Batch Events](actions/send-offline-batch-events.md) | `POST https://tr.snapchat.com/v3/:pixel_id/events` | [docs](https://developers.snap.com/api/marketing-api/Conversions-API/OfflineEvents) |
| [Send Page View Event](actions/send-page-view-event.md) | `POST https://tr.snapchat.com/v3/:asset_id/events` | [docs](https://developers.snap.com/api/marketing-api/Conversions-API/Parameters) |
| [Send Purchase Event](actions/send-purchase-event.md) | `POST https://tr.snapchat.com/v3/:asset_id/events` | [docs](https://developers.snap.com/api/marketing-api/Conversions-API/Parameters) |
| [Send Rate Event](actions/send-rate-event.md) | `POST https://tr.snapchat.com/v3/:asset_id/events` | [docs](https://developers.snap.com/api/marketing-api/Conversions-API/Parameters) |
| [Send Reserve Event](actions/send-reserve-event.md) | `POST https://tr.snapchat.com/v3/:asset_id/events` | [docs](https://developers.snap.com/api/marketing-api/Conversions-API/Parameters) |
| [Send Save Event](actions/send-save-event.md) | `POST https://tr.snapchat.com/v3/:asset_id/events` | [docs](https://developers.snap.com/api/marketing-api/Conversions-API/Parameters) |
| [Send Search Event](actions/send-search-event.md) | `POST https://tr.snapchat.com/v3/:asset_id/events` | [docs](https://developers.snap.com/api/marketing-api/Conversions-API/Parameters) |
| [Send Share Event](actions/send-share-event.md) | `POST https://tr.snapchat.com/v3/:asset_id/events` | [docs](https://developers.snap.com/api/marketing-api/Conversions-API/Parameters) |
| [Send Sign Up Event](actions/send-sign-up-event.md) | `POST https://tr.snapchat.com/v3/:asset_id/events` | [docs](https://developers.snap.com/api/marketing-api/Conversions-API/Parameters) |
| [Send Spent Credits Event](actions/send-spent-credits-event.md) | `POST https://tr.snapchat.com/v3/:asset_id/events` | [docs](https://developers.snap.com/api/marketing-api/Conversions-API/Parameters) |
| [Send Start Checkout Event](actions/send-start-checkout-event.md) | `POST https://tr.snapchat.com/v3/:asset_id/events` | [docs](https://developers.snap.com/api/marketing-api/Conversions-API/Parameters) |
| [Send Start Trial Event](actions/send-start-trial-event.md) | `POST https://tr.snapchat.com/v3/:asset_id/events` | [docs](https://developers.snap.com/api/marketing-api/Conversions-API/Parameters) |
| [Send Subscribe Event](actions/send-subscribe-event.md) | `POST https://tr.snapchat.com/v3/:asset_id/events` | [docs](https://developers.snap.com/api/marketing-api/Conversions-API/Parameters) |
| [Send View Content Event](actions/send-view-content-event.md) | `POST https://tr.snapchat.com/v3/:asset_id/events` | [docs](https://developers.snap.com/api/marketing-api/Conversions-API/Parameters) |
| [Send Web Batch Events](actions/send-web-batch-events.md) | `POST https://tr.snapchat.com/v3/:pixel_id/events` | [docs](https://developers.snap.com/api/marketing-api/Conversions-API/UsingTheAPI) |
| [Validate Test Events](actions/validate-test-events.md) | `POST https://tr.snapchat.com/v3/:asset_id/events/validate` | [docs](https://developers.snap.com/api/marketing-api/Conversions-API/VerifySetUp) |
