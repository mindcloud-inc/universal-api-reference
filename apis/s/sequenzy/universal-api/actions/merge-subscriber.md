# Sequenzy: Merge Subscriber

Creates or merges a subscriber in Sequenzy by email.

```
POST https://connect.mindcloud.co/v1/universal/sequenzy/latest/actions/merge-subscriber
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Sequenzy `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/sequenzy/latest/actions/merge-subscriber" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "email": "ava@example.com"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/sequenzy/latest/actions/merge-subscriber', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "email": "ava@example.com"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `email` | string | yes | Subscriber email address. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "subscriber": {
        "created": true,
        "createdAt": "string",
        "customAttributes": {},
        "email": "ava@example.com",
        "firstName": "Ava",
        "id": "string",
        "lastName": "Chen",
        "skipped": true,
        "status": "string",
        "tags": [
          "string"
        ],
        "updated": true
      },
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `subscriber.created` | boolean |  |
| `subscriber.createdAt` | string |  |
| `subscriber.customAttributes` | object |  |
| `subscriber.email` | string |  |
| `subscriber.firstName` | string |  |
| `subscriber.id` | string |  |
| `subscriber.lastName` | string |  |
| `subscriber.skipped` | boolean |  |
| `subscriber.status` | string |  |
| `subscriber.tags` | array<string> |  |
| `subscriber.updated` | boolean |  |
| `success` | boolean |  |

## Native endpoint

Through the native Sequenzy API, this operation is `POST /subscribers` (base URL `https://api.sequenzy.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/merge-subscriber.md) for the provider-specific parameters and requirements.

