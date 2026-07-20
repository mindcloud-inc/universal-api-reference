# Vybit: Send Notification to Owner



```
POST https://connect.mindcloud.co/v1/universal/vybit/latest/actions/send-notification-to-owner
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Vybit `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/vybit/latest/actions/send-notification-to-owner" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/vybit/latest/actions/send-notification-to-owner', {
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

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `imageUrl` | string | no | Custom image URL |
| `key` | string | no | The unique key of the subscription following record. |
| `linkUrl` | string | no | Custom link URL |
| `message` | string | no | Notification message |

## Response

```json
{
  "success": true,
  "data": [
    {
      "plk": "string",
      "result": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `plk` | string |  |
| `result` | number |  |

## Native endpoint

Through the native Vybit API, this operation is `POST /subscription/following/{{key}}/send-to-owner` (base URL `https://api.vybit.net/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/send-notification-to-owner.md) for the provider-specific parameters and requirements.

