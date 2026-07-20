# Update Webhook with Fourthwall

Updates an existing webhook in Fourthwall.

## Endpoint

- **Method:** `PUT`
- **Path:** `/open-api/v1.0/webhooks/:webhookConfigurationId`
- **Base URL:** `https://api.fourthwall.com`
- **Official documentation:** [Update Webhook](https://docs.fourthwall.com/api-reference/platform/webhooks/update-webhook)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `webhookConfigurationId` | path | `string` | yes | The webhook configuration ID. |
| `url` | body | `string` | yes | The webhook destination URL. |
| `allowedTypes[]` | body | `array<string>` | yes | Array of webhook event types to subscribe to. Accepted values: `CART_ABANDONED_1H`, `CART_ABANDONED_24H`, `CART_ABANDONED_72H`, `COLLECTION_UPDATED`, `DONATION`, `GIFT_DRAW_ENDED`, `GIFT_DRAW_STARTED`, `GIFT_PURCHASE`, `MEMBERSHIP_POST_UPSERTED`, `MEMBERSHIP_SERIES_DELETED`, `MEMBERSHIP_SERIES_UPSERTED`, `MEMBERSHIP_TAG_CREATED`, `MEMBERSHIP_TIER_DELETED`, `MEMBERSHIP_TIER_UPSERTED`, `NEWSLETTER_SUBSCRIBED`, `ORDER_PLACED`, `ORDER_UPDATED`, `PLATFORM_APP_DISCONNECTED`, `PRODUCT_CREATED`, `PRODUCT_UPDATED`, `PROMOTION_CREATED`, `PROMOTION_STATUS_CHANGED`, `PROMOTION_UPDATED`, `SUBSCRIPTION_CHANGED`, `SUBSCRIPTION_EXPIRED`, `SUBSCRIPTION_PURCHASED`, `THANK_YOU_SENT`. |
