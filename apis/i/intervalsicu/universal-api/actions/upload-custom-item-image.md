# Intervals.icu: Upload Custom Item Image

Uploads a custom item image to Intervals.icu.

```
POST https://connect.mindcloud.co/v1/universal/intervalsicu/latest/actions/upload-custom-item-image
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Intervals.icu `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/intervalsicu/latest/actions/upload-custom-item-image" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/intervalsicu/latest/actions/upload-custom-item-image', {
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

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Intervals.icu API returns.

## Native endpoint

Through the native Intervals.icu API, this operation is `POST /api/v1/athlete/:id/custom-item/:itemId/image` (base URL `https://intervals.icu`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/upload-custom-item-image.md) for the provider-specific parameters and requirements.

