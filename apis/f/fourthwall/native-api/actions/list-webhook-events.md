# List Webhook Events with Fourthwall

Retrieves webhook events from Fourthwall with optional type filtering.

## Endpoint

- **Method:** `GET`
- **Path:** `/open-api/v1.0/webhook-events`
- **Base URL:** `https://api.fourthwall.com`
- **Official documentation:** [List Webhook Events](https://docs.fourthwall.com/api-reference/platform/webhooks/list-webhook-events)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `type` | query | `list` | no | Filter webhook events by type. Accepted values: `CART_ABANDONED_1H`, `CART_ABANDONED_24H`, `CART_ABANDONED_72H`, `COLLECTION_UPDATED`, `DONATION`, `GIFT_DRAW_ENDED`, `GIFT_DRAW_STARTED`, `GIFT_PURCHASE`, `MEMBERSHIP_POST_UPSERTED`, `MEMBERSHIP_SERIES_DELETED`, `MEMBERSHIP_SERIES_UPSERTED`, `MEMBERSHIP_TAG_CREATED`, `MEMBERSHIP_TIER_DELETED`, `MEMBERSHIP_TIER_UPSERTED`, `NEWSLETTER_SUBSCRIBED`, `ORDER_PLACED`, `ORDER_UPDATED`, `PLATFORM_APP_DISCONNECTED`, `PRODUCT_CREATED`, `PRODUCT_UPDATED`, `PROMOTION_CREATED`, `PROMOTION_STATUS_CHANGED`, `PROMOTION_UPDATED`, `SUBSCRIPTION_CHANGED`, `SUBSCRIPTION_EXPIRED`, `SUBSCRIPTION_PURCHASED`, `THANK_YOU_SENT`. |
