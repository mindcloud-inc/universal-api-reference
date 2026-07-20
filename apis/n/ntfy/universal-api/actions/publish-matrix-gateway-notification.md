# ntfy: Publish Matrix Gateway Notification

Publishes a Matrix gateway notification through ntfy.

```
POST https://connect.mindcloud.co/v1/universal/ntfy/latest/actions/publish-matrix-gateway-notification
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ntfy `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/ntfy/latest/actions/publish-matrix-gateway-notification" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/ntfy/latest/actions/publish-matrix-gateway-notification', {
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

```json
{
  "success": true,
  "data": [
    {
      "rejected": [
        "string"
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `rejected` | array<string> | Matrix pushkeys rejected by the gateway response. |

## Native endpoint

Through the native ntfy API, this operation is `POST /_matrix/push/v1/notify` (base URL `https://ntfy.sh`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/publish-matrix-gateway-notification.md) for the provider-specific parameters and requirements.

