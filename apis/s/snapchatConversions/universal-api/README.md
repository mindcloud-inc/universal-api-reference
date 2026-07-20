# <img src="https://images.mindcloud.co/apps/icons/icon-1_1775677480126.jpeg" alt="Snapchat Conversions logo" width="28" height="28"> Snapchat Conversions: Universal API

Send Snapchat conversion events and review signal quality

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/snapchatConversions/latest
- **Category:** Marketing / Advertising
- **Actions:** 40
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://forbusiness.snapchat.com
- **Vendor API docs:** https://developers.snap.com/api/marketing-api/Conversions-API/Introduction

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get App Signal Readiness Scores](actions/get-app-signal-readiness-scores.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/snapchatConversions/latest/actions/get-app-signal-readiness-scores?connectionId=$CONNECTION_ID&snapAppId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (40)

### Achievement Unlocked Event Result

| Action | Method | Description |
| --- | --- | --- |
| [Send Achievement Unlocked Event](actions/send-achievement-unlocked-event.md) | POST | Creates an achievement unlocked conversion event in Snapchat Conversions. |

### Ad Click Event Result

| Action | Method | Description |
| --- | --- | --- |
| [Send Ad Click Event](actions/send-ad-click-event.md) | POST | Creates an ad click conversion event in Snapchat Conversions. |

### Ad View Event Result

| Action | Method | Description |
| --- | --- | --- |
| [Send Ad View Event](actions/send-ad-view-event.md) | POST | Creates an ad view conversion event in Snapchat Conversions. |

### Add Billing Event Result

| Action | Method | Description |
| --- | --- | --- |
| [Send Add Billing Event](actions/send-add-billing-event.md) | POST | Creates an add billing conversion event in Snapchat Conversions. |

### Add Cart Event Result

| Action | Method | Description |
| --- | --- | --- |
| [Send Add Cart Event](actions/send-add-cart-event.md) | POST | Creates an add cart conversion event in Snapchat Conversions. |

### Add To Wishlist Event Result

| Action | Method | Description |
| --- | --- | --- |
| [Send Add To Wishlist Event](actions/send-add-to-wishlist-event.md) | POST | Creates an add-to-wishlist conversion event in Snapchat Conversions. |

### App Batch Event Result

| Action | Method | Description |
| --- | --- | --- |
| [Send App Batch Events](actions/send-app-batch-events.md) | POST | Creates a batch of app conversion events in Snapchat Conversions. |

### App Install Event Result

| Action | Method | Description |
| --- | --- | --- |
| [Send App Install Event](actions/send-app-install-event.md) | POST | Creates an app install conversion event in Snapchat Conversions. |

### App Open Event Result

| Action | Method | Description |
| --- | --- | --- |
| [Send App Open Event](actions/send-app-open-event.md) | POST | Creates an app open conversion event in Snapchat Conversions. |

### App Signal Readiness Score

| Action | Method | Description |
| --- | --- | --- |
| [Get App Signal Readiness Scores](actions/get-app-signal-readiness-scores.md) | GET | Retrieves app signal readiness scores in Snapchat Conversions. |

### Complete Tutorial Event Result

| Action | Method | Description |
| --- | --- | --- |
| [Send Complete Tutorial Event](actions/send-complete-tutorial-event.md) | POST | Creates a complete tutorial conversion event in Snapchat Conversions. |

### Custom Event 1 Result

| Action | Method | Description |
| --- | --- | --- |
| [Send Custom Event 1](actions/send-custom-event1.md) | POST | Creates a CUSTOM_EVENT_1 conversion event in Snapchat Conversions. |

### Custom Event 2 Result

| Action | Method | Description |
| --- | --- | --- |
| [Send Custom Event 2](actions/send-custom-event2.md) | POST | Creates a CUSTOM_EVENT_2 conversion event in Snapchat Conversions. |

### Custom Event 3 Result

| Action | Method | Description |
| --- | --- | --- |
| [Send Custom Event 3](actions/send-custom-event3.md) | POST | Creates a CUSTOM_EVENT_3 conversion event in Snapchat Conversions. |

### Custom Event 4 Result

| Action | Method | Description |
| --- | --- | --- |
| [Send Custom Event 4](actions/send-custom-event4.md) | POST | Creates a CUSTOM_EVENT_4 conversion event in Snapchat Conversions. |

### Custom Event 5 Result

| Action | Method | Description |
| --- | --- | --- |
| [Send Custom Event 5](actions/send-custom-event5.md) | POST | Creates a CUSTOM_EVENT_5 conversion event in Snapchat Conversions. |

### Invite Event Result

| Action | Method | Description |
| --- | --- | --- |
| [Send Invite Event](actions/send-invite-event.md) | POST | Creates an invite conversion event in Snapchat Conversions. |

### Level Complete Event Result

| Action | Method | Description |
| --- | --- | --- |
| [Send Level Complete Event](actions/send-level-complete-event.md) | POST | Creates a level complete conversion event in Snapchat Conversions. |

### List View Event Result

| Action | Method | Description |
| --- | --- | --- |
| [Send List View Event](actions/send-list-view-event.md) | POST | Creates a list view conversion event in Snapchat Conversions. |

### Login Event Result

| Action | Method | Description |
| --- | --- | --- |
| [Send Login Event](actions/send-login-event.md) | POST | Creates a login conversion event in Snapchat Conversions. |

### Mixed Event Batch Result

| Action | Method | Description |
| --- | --- | --- |
| [Send Mixed Event Batch](actions/send-mixed-event-batch.md) | POST | Creates a batch of web or app conversion events in Snapchat Conversions. |

### Offline Batch Event Result

| Action | Method | Description |
| --- | --- | --- |
| [Send Offline Batch Events](actions/send-offline-batch-events.md) | POST | Creates a batch of offline conversion events in Snapchat Conversions. |

### Page View Event Result

| Action | Method | Description |
| --- | --- | --- |
| [Send Page View Event](actions/send-page-view-event.md) | POST | Creates a page view conversion event in Snapchat Conversions. |

### Pixel Signal Readiness Score

| Action | Method | Description |
| --- | --- | --- |
| [Get Pixel Signal Readiness Scores](actions/get-pixel-signal-readiness-scores.md) | GET | Retrieves pixel signal readiness scores in Snapchat Conversions. |

### Purchase Event Result

| Action | Method | Description |
| --- | --- | --- |
| [Send Purchase Event](actions/send-purchase-event.md) | POST | Creates a purchase conversion event in Snapchat Conversions. |

### Rate Event Result

| Action | Method | Description |
| --- | --- | --- |
| [Send Rate Event](actions/send-rate-event.md) | POST | Creates a rate conversion event in Snapchat Conversions. |

### Reserve Event Result

| Action | Method | Description |
| --- | --- | --- |
| [Send Reserve Event](actions/send-reserve-event.md) | POST | Creates a reserve conversion event in Snapchat Conversions. |

### Save Event Result

| Action | Method | Description |
| --- | --- | --- |
| [Send Save Event](actions/send-save-event.md) | POST | Creates a save conversion event in Snapchat Conversions. |

### Search Event Result

| Action | Method | Description |
| --- | --- | --- |
| [Send Search Event](actions/send-search-event.md) | POST | Creates a search conversion event in Snapchat Conversions. |

### Share Event Result

| Action | Method | Description |
| --- | --- | --- |
| [Send Share Event](actions/send-share-event.md) | POST | Creates a share conversion event in Snapchat Conversions. |

### Sign Up Event Result

| Action | Method | Description |
| --- | --- | --- |
| [Send Sign Up Event](actions/send-sign-up-event.md) | POST | Creates a sign up conversion event in Snapchat Conversions. |

### Spent Credits Event Result

| Action | Method | Description |
| --- | --- | --- |
| [Send Spent Credits Event](actions/send-spent-credits-event.md) | POST | Creates a spent credits conversion event in Snapchat Conversions. |

### Start Checkout Event Result

| Action | Method | Description |
| --- | --- | --- |
| [Send Start Checkout Event](actions/send-start-checkout-event.md) | POST | Creates a start checkout conversion event in Snapchat Conversions. |

### Start Trial Event Result

| Action | Method | Description |
| --- | --- | --- |
| [Send Start Trial Event](actions/send-start-trial-event.md) | POST | Creates a start trial conversion event in Snapchat Conversions. |

### Subscribe Event Result

| Action | Method | Description |
| --- | --- | --- |
| [Send Subscribe Event](actions/send-subscribe-event.md) | POST | Creates a subscribe conversion event in Snapchat Conversions. |

### Test Event Log

| Action | Method | Description |
| --- | --- | --- |
| [Get Test Event Logs](actions/get-test-event-logs.md) | GET | Retrieves test event logs in Snapchat Conversions. |

### Test Event Stat

| Action | Method | Description |
| --- | --- | --- |
| [Get Test Event Stats](actions/get-test-event-stats.md) | GET | Retrieves test event stats in Snapchat Conversions. |

### Test Event Validation

| Action | Method | Description |
| --- | --- | --- |
| [Validate Test Events](actions/validate-test-events.md) | GET | Validates test conversion events in Snapchat Conversions. |

### View Content Event Result

| Action | Method | Description |
| --- | --- | --- |
| [Send View Content Event](actions/send-view-content-event.md) | POST | Creates a view content conversion event in Snapchat Conversions. |

### Web Batch Event Result

| Action | Method | Description |
| --- | --- | --- |
| [Send Web Batch Events](actions/send-web-batch-events.md) | POST | Creates a batch of web conversion events in Snapchat Conversions. |

