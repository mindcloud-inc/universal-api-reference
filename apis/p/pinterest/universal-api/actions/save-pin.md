# Pinterest: Save Pin

Saves a pin to a Pinterest board or section.

```
POST https://connect.mindcloud.co/v1/universal/pinterest/latest/actions/save-pin
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Pinterest `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/pinterest/latest/actions/save-pin" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/pinterest/latest/actions/save-pin', {
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

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Pinterest API returns.

## Native endpoint

Through the native Pinterest API, this operation is `POST pins/:pinId/save` (base URL `https://api.pinterest.com/v5`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/save-pin.md) for the provider-specific parameters and requirements.

