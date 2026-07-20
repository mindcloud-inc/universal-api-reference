# BlueFox Email: Subscribe

Subscribes a contact to a BlueFox Email list.

```
POST https://connect.mindcloud.co/v1/universal/blueFoxEmail/latest/actions/subscribe
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a BlueFox Email `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/blueFoxEmail/latest/actions/subscribe" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "subscriberListId": "string",
  "email": "ava@example.com"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/blueFoxEmail/latest/actions/subscribe', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "subscriberListId": "string",
    "email": "ava@example.com"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `subscriberListId` | string | yes | BlueFox subscriber list ID. |
| `email` | string | yes | Email address to subscribe. |
| `name` | string | no | Name of the subscriber. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "__v": 1,
      "_id": "string",
      "accountId": "string",
      "createdAt": "2026-05-07T12:00:00.000Z",
      "email": "ava@example.com",
      "projectId": "string",
      "status": "string",
      "subscriberListId": "string",
      "tags": [
        "string"
      ],
      "updatedAt": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `__v` | number |  |
| `_id` | string |  |
| `accountId` | string |  |
| `createdAt` | date |  |
| `email` | string |  |
| `projectId` | string |  |
| `status` | string |  |
| `subscriberListId` | string |  |
| `tags` | array<string> |  |
| `updatedAt` | date |  |

## Native endpoint

Through the native BlueFox Email API, this operation is `POST /v1/subscriber-lists/:subscriberListId` (base URL `https://api.bluefox.email`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/subscribe.md) for the provider-specific parameters and requirements.

