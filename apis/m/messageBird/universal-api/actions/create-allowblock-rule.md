# MessageBird: Create Allow/Block Rule



```
POST https://connect.mindcloud.co/v1/universal/messageBird/latest/actions/create-allowblock-rule
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a MessageBird `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/messageBird/latest/actions/create-allowblock-rule" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "workspaceId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/messageBird/latest/actions/create-allowblock-rule', {
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
| `workspaceId` | string | yes | The Bird workspace ID where the allow/block rule should be created. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "category": "string",
      "createdAt": "2026-05-07T12:00:00.000Z",
      "createdBy": "string",
      "id": "string",
      "type": "string",
      "updatedAt": "2026-05-07T12:00:00.000Z",
      "updatedBy": "string",
      "value": "string",
      "workspaceId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `category` | string | The category of the AllowBlockRule. |
| `createdAt` | date |  |
| `createdBy` | string |  |
| `id` | string |  |
| `type` | string | The type of the AllowBlockRule. |
| `updatedAt` | date |  |
| `updatedBy` | string |  |
| `value` | string |  |
| `workspaceId` | string |  |

## Native endpoint

Through the native MessageBird API, this operation is `POST /workspaces/:workspaceId/conversation-allowblock-rules` (base URL `https://api.bird.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-allowblock-rule.md) for the provider-specific parameters and requirements.

