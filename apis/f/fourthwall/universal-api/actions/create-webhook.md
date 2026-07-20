# Fourthwall: Create Webhook

Creates a new webhook in Fourthwall.

```
POST https://connect.mindcloud.co/v1/universal/fourthwall/latest/actions/create-webhook
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Fourthwall `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/fourthwall/latest/actions/create-webhook" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "url": "https://example.com",
  "allowedTypes[]": "CART_ABANDONED_1H"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/fourthwall/latest/actions/create-webhook', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "url": "https://example.com",
    "allowedTypes[]": "CART_ABANDONED_1H"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `url` | string | yes | The webhook destination URL. |
| `allowedTypes[]` | array<string> | yes | Array of webhook event types to subscribe to. One of: `CART_ABANDONED_1H`, `CART_ABANDONED_24H`, `CART_ABANDONED_72H`, `COLLECTION_UPDATED`, `DONATION`, `GIFT_DRAW_ENDED`, `GIFT_DRAW_STARTED`, `GIFT_PURCHASE`, `MEMBERSHIP_POST_UPSERTED`, `MEMBERSHIP_SERIES_DELETED`, `MEMBERSHIP_SERIES_UPSERTED`, `MEMBERSHIP_TAG_CREATED`, `MEMBERSHIP_TIER_DELETED`, `MEMBERSHIP_TIER_UPSERTED`, `NEWSLETTER_SUBSCRIBED`, `ORDER_PLACED`, `ORDER_UPDATED`, `PLATFORM_APP_DISCONNECTED`, `PRODUCT_CREATED`, `PRODUCT_UPDATED`, `PROMOTION_CREATED`, `PROMOTION_STATUS_CHANGED`, `PROMOTION_UPDATED`, `SUBSCRIPTION_CHANGED`, `SUBSCRIPTION_EXPIRED`, `SUBSCRIPTION_PURCHASED`, `THANK_YOU_SENT`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "allowedTypes": [
        "string"
      ],
      "apiVersion": "string",
      "id": "string",
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `allowedTypes[]` | string |  |
| `apiVersion` | string |  |
| `id` | string |  |
| `url` | string |  |

## Native endpoint

Through the native Fourthwall API, this operation is `POST /open-api/v1.0/webhooks` (base URL `https://api.fourthwall.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-webhook.md) for the provider-specific parameters and requirements.

