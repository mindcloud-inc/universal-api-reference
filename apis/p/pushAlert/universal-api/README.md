# <img src="https://images.mindcloud.co/apps/icons/push-alert_1774304314418.png" alt="PushAlert logo" width="28" height="28"> PushAlert: Universal API

Send, segment, and automate web push notifications

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/pushAlert/latest
- **Category:** Marketing
- **Actions:** 16
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://pushalert.co
- **Vendor API docs:** https://pushalert.co/documentation/rest-api-v2/web-push

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get All Segments](actions/get-all-segments.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/pushAlert/latest/actions/get-all-segments?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (16)

### Carts

| Action | Method | Description |
| --- | --- | --- |
| [Delete Abandoned Cart Notification](actions/delete-abandoned-cart-notification.md) | DELETE |  |
| [Schedule Abandoned Cart Notification](actions/schedule-abandoned-cart-notification.md) | POST |  |

### Events

| Action | Method | Description |
| --- | --- | --- |
| [Track Subscriber Event](actions/track-subscriber-event.md) | POST |  |

### Notifications

| Action | Method | Description |
| --- | --- | --- |
| [Delete Scheduled Notification](actions/delete-scheduled-notification.md) | DELETE |  |
| [Get Notification Info](actions/get-notification-info.md) | GET |  |
| [Send Notification](actions/send-notification.md) | POST |  |
| [Send Notification To Segment](actions/send-notification-to-segment.md) | POST |  |

### Orders

| Action | Method | Description |
| --- | --- | --- |
| [Track Order Shipment](actions/track-order-shipment.md) | PUT |  |

### Products

| Action | Method | Description |
| --- | --- | --- |
| [Update Product Alerts](actions/update-product-alerts.md) | PUT |  |

### Segments

| Action | Method | Description |
| --- | --- | --- |
| [Add Subscribers To Segment](actions/add-subscribers-to-segment.md) | PUT |  |
| [Create Segment](actions/create-segment.md) | POST |  |
| [Delete Segment](actions/delete-segment.md) | DELETE |  |
| [Get All Segments](actions/get-all-segments.md) | GET |  |
| [Remove Subscribers From Segment](actions/remove-subscribers-from-segment.md) | PUT |  |

### Subscribers

| Action | Method | Description |
| --- | --- | --- |
| [Add Subscriber Attributes](actions/add-subscriber-attributes.md) | PUT |  |
| [Get Subscriber Attributes](actions/get-subscriber-attributes.md) | GET |  |

