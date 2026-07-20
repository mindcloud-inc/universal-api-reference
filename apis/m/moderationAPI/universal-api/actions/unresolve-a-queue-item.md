# Moderation API: Unresolve A Queue Item

Unresolves a review queue item in Moderation API.

```
PUT https://connect.mindcloud.co/v1/universal/moderationAPI/latest/actions/unresolve-a-queue-item
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Moderation API `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/moderationAPI/latest/actions/unresolve-a-queue-item" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "string",
  "itemId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/moderationAPI/latest/actions/unresolve-a-queue-item', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "string",
    "itemId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | string | yes | The queue ID |
| `itemId` | string | yes | The item ID to unresolve |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `comment` | string | no | Optional reason for unresolving the item |

## Response

```json
{
  "success": true,
  "data": [
    {
      "status": "string",
      "success": true,
      "unresolvedAt": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `status` | string | New status of the item |
| `success` | boolean |  |
| `unresolvedAt` | string | Timestamp when the item was unresolved |

## Native endpoint

Through the native Moderation API API, this operation is `POST /queue/:id/items/:itemId/unresolve` (base URL `https://api.moderationapi.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/unresolve-a-queue-item.md) for the provider-specific parameters and requirements.

