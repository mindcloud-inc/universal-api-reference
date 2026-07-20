# MessageBird: Add Allow/Block Rules in Bulk



```
POST https://connect.mindcloud.co/v1/universal/messageBird/latest/actions/add-allowblock-rules-in-bulk
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a MessageBird `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/messageBird/latest/actions/add-allowblock-rules-in-bulk" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "workspaceId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/messageBird/latest/actions/add-allowblock-rules-in-bulk', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "workspaceId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `workspaceId` | string | yes | The Bird workspace ID where the bulk allow/block upload should run. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "bulkId": "string",
      "currentIndex": 1,
      "errors": [
        "string"
      ],
      "status": "string",
      "total": 1,
      "updatedAt": "2026-05-07T12:00:00.000Z",
      "workspaceId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `bulkId` | string |  |
| `currentIndex` | number |  |
| `errors` | array<string> |  |
| `status` | string |  |
| `total` | number |  |
| `updatedAt` | date |  |
| `workspaceId` | string |  |

## Native endpoint

Through the native MessageBird API, this operation is `POST /workspaces/:workspaceId/conversation-allowblock-rules-bulk` (base URL `https://api.bird.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/add-allowblock-rules-in-bulk.md) for the provider-specific parameters and requirements.

