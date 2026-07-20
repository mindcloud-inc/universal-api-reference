# AssignX: Create Conversation

Creates a new conversation in AssignX.

```
POST https://connect.mindcloud.co/v1/universal/assignX/latest/actions/create-conversation
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a AssignX `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/assignX/latest/actions/create-conversation" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/assignX/latest/actions/create-conversation', {
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
| `id` | string | yes | Agent identifier from List Agents. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "bots": [
        "string"
      ],
      "contextUsage": {
        "contextWindowSize": 1,
        "lastUpdated": "2026-05-07T12:00:00.000Z",
        "messageCount": 1,
        "totalInputTokens": 1,
        "totalOutputTokens": 1,
        "totalTokens": 1,
        "usagePercentage": 1
      },
      "createdAt": "2026-05-07T12:00:00.000Z",
      "hasEnded": true,
      "Id": "string",
      "isPreview": true,
      "isSharedChat": true,
      "lastActivity": "2026-05-07T12:00:00.000Z",
      "name": {},
      "origin": "string",
      "title": {},
      "type": "string",
      "updatedAt": "2026-05-07T12:00:00.000Z",
      "users": [
        "string"
      ],
      "V": 1,
      "vote": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `bots[]` | string |  |
| `contextUsage.contextWindowSize` | number |  |
| `contextUsage.lastUpdated` | date |  |
| `contextUsage.messageCount` | number |  |
| `contextUsage.totalInputTokens` | number |  |
| `contextUsage.totalOutputTokens` | number |  |
| `contextUsage.totalTokens` | number |  |
| `contextUsage.usagePercentage` | number |  |
| `createdAt` | date |  |
| `hasEnded` | boolean |  |
| `Id` | string |  |
| `isPreview` | boolean |  |
| `isSharedChat` | boolean |  |
| `lastActivity` | date |  |
| `name` | object |  |
| `origin` | string |  |
| `title` | object |  |
| `type` | string |  |
| `updatedAt` | date |  |
| `users[]` | string |  |
| `V` | number |  |
| `vote` | object |  |

## Native endpoint

Through the native AssignX API, this operation is `POST agents/:id/conversations/new` (base URL `https://api.agentx.so/api/v1/access/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-conversation.md) for the provider-specific parameters and requirements.

