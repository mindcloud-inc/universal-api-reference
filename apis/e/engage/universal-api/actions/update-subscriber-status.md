# Engage: Update Subscriber Status

Updates a user's subscription status for an Engage list.

```
PUT https://connect.mindcloud.co/v1/universal/engage/latest/actions/update-subscriber-status
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Engage `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/engage/latest/actions/update-subscriber-status" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "string",
  "subscribed": true,
  "uid": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/engage/latest/actions/update-subscriber-status', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "string",
    "subscribed": true,
    "uid": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | string | yes | The Engage list ID. |
| `subscribed` | boolean | yes | Set to true to subscribe or false to unsubscribe the user. |
| `uid` | string | yes | The subscriber user ID from your application. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "subscribed": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `subscribed` | boolean | Whether the subscriber remains subscribed to the list. |

## Native endpoint

Through the native Engage API, this operation is `PUT /lists/:id/subscribers/:uid` (base URL `https://api.engage.so/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-subscriber-status.md) for the provider-specific parameters and requirements.

