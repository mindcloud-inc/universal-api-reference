# Snapchat Conversions: Send Add To Wishlist Event

Creates an add-to-wishlist conversion event in Snapchat Conversions.

```
POST https://connect.mindcloud.co/v1/universal/snapchatConversions/latest/actions/send-add-to-wishlist-event
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Snapchat Conversions `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/snapchatConversions/latest/actions/send-add-to-wishlist-event" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/snapchatConversions/latest/actions/send-add-to-wishlist-event', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```



## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Snapchat Conversions API returns.

## Native endpoint

Through the native Snapchat Conversions API, this operation is `POST https://tr.snapchat.com/v3/:asset_id/events` (base URL `https://adsapi.snapchat.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/send-add-to-wishlist-event.md) for the provider-specific parameters and requirements.

