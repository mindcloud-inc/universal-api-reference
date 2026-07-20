# Fourthwall: List Webhook Events

Retrieves webhook events from Fourthwall with optional type filtering.

```
GET https://connect.mindcloud.co/v1/universal/fourthwall/latest/actions/list-webhook-events
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Fourthwall `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/fourthwall/latest/actions/list-webhook-events?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/fourthwall/latest/actions/list-webhook-events?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as query string parameters ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `type` | list | no | Filter webhook events by type. One of: `CART_ABANDONED_1H`, `CART_ABANDONED_24H`, `CART_ABANDONED_72H`, `COLLECTION_UPDATED`, `DONATION`, `GIFT_DRAW_ENDED`, `GIFT_DRAW_STARTED`, `GIFT_PURCHASE`, `MEMBERSHIP_POST_UPSERTED`, `MEMBERSHIP_SERIES_DELETED`, `MEMBERSHIP_SERIES_UPSERTED`, `MEMBERSHIP_TAG_CREATED`, `MEMBERSHIP_TIER_DELETED`, `MEMBERSHIP_TIER_UPSERTED`, `NEWSLETTER_SUBSCRIBED`, `ORDER_PLACED`, `ORDER_UPDATED`, `PLATFORM_APP_DISCONNECTED`, `PRODUCT_CREATED`, `PRODUCT_UPDATED`, `PROMOTION_CREATED`, `PROMOTION_STATUS_CHANGED`, `PROMOTION_UPDATED`, `SUBSCRIPTION_CHANGED`, `SUBSCRIPTION_EXPIRED`, `SUBSCRIPTION_PURCHASED`, `THANK_YOU_SENT`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "apiVersion": "string",
      "body": "string",
      "createdAt": "2026-05-07T12:00:00.000Z",
      "error": "string",
      "id": "string",
      "state": "string",
      "testMode": true,
      "type": "string",
      "updatedAt": "2026-05-07T12:00:00.000Z",
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `apiVersion` | string |  |
| `body` | string |  |
| `createdAt` | date |  |
| `error` | string |  |
| `id` | string |  |
| `state` | string |  |
| `testMode` | boolean |  |
| `type` | string |  |
| `updatedAt` | date |  |
| `url` | string |  |

## Native endpoint

Through the native Fourthwall API, this operation is `GET /open-api/v1.0/webhook-events` (base URL `https://api.fourthwall.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-webhook-events.md) for the provider-specific parameters and requirements.

