# LoopedIn: Subscribe to Updates

Subscribes a user to updates in LoopedIn.

```
POST https://connect.mindcloud.co/v1/universal/loopedIn/latest/actions/subscribe-to-updates
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a LoopedIn `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/loopedIn/latest/actions/subscribe-to-updates" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "email": "ava@example.com",
  "workspace_id": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/loopedIn/latest/actions/subscribe-to-updates', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "email": "ava@example.com",
    "workspace_id": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `email` | string | yes | The subscriber email address. |
| `name` | string | no | The subscriber name. |
| `workspace_id` | string | yes | The LoopedIn workspace ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "email": "ava@example.com",
      "followed": true,
      "name": "Ava Chen",
      "optInRequired": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `email` | string |  |
| `followed` | boolean |  |
| `name` | string |  |
| `optInRequired` | boolean |  |

## Native endpoint

Through the native LoopedIn API, this operation is `POST /updates/public-subscribe` (base URL `https://api.loopedin.io/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/subscribe-to-updates.md) for the provider-specific parameters and requirements.

