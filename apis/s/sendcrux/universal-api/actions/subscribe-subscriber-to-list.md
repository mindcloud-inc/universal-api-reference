# Sendcrux: Subscribe Subscriber to List

Updates a Sendcrux subscriber by subscribing them to a list.

```
PUT https://connect.mindcloud.co/v1/universal/sendcrux/latest/actions/subscribe-subscriber-to-list
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Sendcrux `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/sendcrux/latest/actions/subscribe-subscriber-to-list" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "list_uid": "string",
  "uid": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/sendcrux/latest/actions/subscribe-subscriber-to-list', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "list_uid": "string",
    "uid": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `list_uid` | string | yes | The unique identifier of the parent list. |
| `uid` | string | yes | The unique identifier of the subscriber to subscribe. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "code": "string",
      "data": {},
      "message": "string",
      "name": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `code` | string |  |
| `data` | object |  |
| `message` | string |  |
| `name` | string |  |

## Native endpoint

Through the native Sendcrux API, this operation is `PATCH /api/v1/lists/:list_uid/subscribers/:uid/subscribe` (base URL `https://sendcrux.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/subscribe-subscriber-to-list.md) for the provider-specific parameters and requirements.

