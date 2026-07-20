# Alltius: Rate Response

Updates feedback for an Alltius assistant response.

```
PUT https://connect.mindcloud.co/v1/universal/alltius/latest/actions/rate-response
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Alltius `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/alltius/latest/actions/rate-response" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "postId": "69d8f8f9d221c6bbc7c37d70",
  "rating": "1"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/alltius/latest/actions/rate-response', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "postId": "69d8f8f9d221c6bbc7c37d70",
    "rating": "1"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `postId` | string | yes | Example: `69d8f8f9d221c6bbc7c37d70`. |
| `rating` | number | yes | Use 1 for thumbs up or -1 for thumbs down. Example: `1`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `success` | boolean | Whether the rating update succeeded. |

## Native endpoint

Through the native Alltius API, this operation is `PUT /v1/chat/rating` (base URL `https://app.alltius.ai/api/platform`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/rate-response.md) for the provider-specific parameters and requirements.

