# Engage: Subscribe User to List

Subscribes a user to a list in Engage, creating them if needed.

```
POST https://connect.mindcloud.co/v1/universal/engage/latest/actions/subscribe-user-to-list
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Engage `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/engage/latest/actions/subscribe-user-to-list" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/engage/latest/actions/subscribe-user-to-list', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `createdAt` | string | no | The creation date for the subscriber. |
| `email` | string | no | The subscriber’s email address. |
| `firstName` | string | no | The subscriber’s first name. |
| `id` | string | yes | The Engage list ID. |
| `lastName` | string | no | The subscriber’s last name. |
| `meta` | object | no | Additional subscriber attributes as an object. |
| `number` | string | no | The subscriber’s phone number in international format. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "uid": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `uid` | string | Identifier returned for the subscribed user record. |

## Native endpoint

Through the native Engage API, this operation is `POST /lists/:id/subscribers` (base URL `https://api.engage.so/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/subscribe-user-to-list.md) for the provider-specific parameters and requirements.

