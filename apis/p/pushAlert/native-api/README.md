# PushAlert: Native API Reference

A consolidated summary of PushAlert's API configuration and 16 documented operations, with links to official documentation.

- **Official docs:** https://pushalert.co/documentation/rest-api-v2/web-push
- **API base URL:** `https://api.pushalert.co`

## Authentication

### API Key

Authenticate PushAlert API requests with an API key.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://pushalert.co/documentation/rest-api-v2/web-push)

## API conventions

Request bodies use URL-encoded form data.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/x-www-form-urlencoded` |

## Endpoints (16 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Add Subscriber Attributes](actions/add-subscriber-attributes.md) | `POST /rest/v2/web-push/attribute/put` | [docs](https://pushalert.co/documentation/rest-api-v2/web-push#rest-api-add-attributes) |
| [Add Subscribers To Segment](actions/add-subscribers-to-segment.md) | `POST /rest/v2/web-push/segment/:segId/add` | [docs](https://pushalert.co/documentation/rest-api-v2/web-push#rest-api-segment-add-subscribers) |
| [Create Segment](actions/create-segment.md) | `POST /rest/v2/web-push/segment/create` | [docs](https://pushalert.co/documentation/rest-api-v2/web-push#rest-api-segment-create) |
| [Delete Abandoned Cart Notification](actions/delete-abandoned-cart-notification.md) | `POST /rest/v2/web-push/abandonedCart/delete` | [docs](https://pushalert.co/documentation/rest-api-v2/web-push#rest-api-abandoned-cart-delete) |
| [Delete Scheduled Notification](actions/delete-scheduled-notification.md) | `POST /rest/v2/web-push/delete/:id` | [docs](https://pushalert.co/documentation/rest-api-v2/web-push#rest-api-notification-delete) |
| [Delete Segment](actions/delete-segment.md) | `POST /rest/v2/web-push/segment/delete` | [docs](https://pushalert.co/documentation/rest-api-v2/web-push#rest-api-segment-delete) |
| [Get All Segments](actions/get-all-segments.md) | `GET /rest/v2/web-push/segments` | [docs](https://pushalert.co/documentation/rest-api-v2/web-push#rest-api-segment-view-all) |
| [Get Notification Info](actions/get-notification-info.md) | `GET /rest/v2/web-push/info/:id` | [docs](https://pushalert.co/documentation/rest-api-v2/web-push#rest-api-notification-info) |
| [Get Subscriber Attributes](actions/get-subscriber-attributes.md) | `POST /rest/v2/web-push/attribute/get` | [docs](https://pushalert.co/documentation/rest-api-v2/web-push#rest-api-get-attributes) |
| [Remove Subscribers From Segment](actions/remove-subscribers-from-segment.md) | `POST /rest/v2/web-push/segment/:segId/remove` | [docs](https://pushalert.co/documentation/rest-api-v2/web-push#rest-api-segment-remove-subscribers) |
| [Schedule Abandoned Cart Notification](actions/schedule-abandoned-cart-notification.md) | `POST /rest/v2/web-push/abandonedCart` | [docs](https://pushalert.co/documentation/rest-api-v2/web-push#rest-api-abandoned-cart-add) |
| [Send Notification](actions/send-notification.md) | `POST /rest/v2/web-push/send` | [docs](https://pushalert.co/documentation/rest-api-v2/web-push#rest-api-send-notification) |
| [Send Notification To Segment](actions/send-notification-to-segment.md) | `POST /rest/v2/web-push/segment/:segId/send` | [docs](https://pushalert.co/documentation/rest-api-v2/web-push#rest-api-segment-send-notification) |
| [Track Order Shipment](actions/track-order-shipment.md) | `POST /rest/v2/web-push/order/track` | [docs](https://pushalert.co/documentation/rest-api-v2/web-push#rest-api-shipment-notifications) |
| [Track Subscriber Event](actions/track-subscriber-event.md) | `POST /rest/v2/web-push/track/event` | [docs](https://pushalert.co/documentation/rest-api-v2/web-push#rest-api-custom-events) |
| [Update Product Alerts](actions/update-product-alerts.md) | `POST /rest/v2/web-push/product/update` | [docs](https://pushalert.co/documentation/rest-api-v2/web-push#rest-api-price-drop-in-stock-alerts) |
