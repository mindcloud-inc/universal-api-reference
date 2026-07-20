# ChatBot: Create User Entity

Creates a new user entity in ChatBot.

```
POST https://connect.mindcloud.co/v1/universal/chatBot/latest/actions/create-user-entity
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ChatBot `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/chatBot/latest/actions/create-user-entity" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "Codex Test Entity 2026-03-18",
  "entries[]": [
    {}
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/chatBot/latest/actions/create-user-entity', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "name": "Codex Test Entity 2026-03-18",
    "entries[]": [{}]
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `name` | string | yes | Entity name. Example: `Codex Test Entity 2026-03-18`. |
| `entries[]` | array<object> | yes | Entity entries array. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": "string",
      "status": {},
      "timestamp": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | string |  |
| `status` | object |  |
| `timestamp` | date |  |

## Native endpoint

Through the native ChatBot API, this operation is `POST /entities` (base URL `https://api.chatbot.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-user-entity.md) for the provider-specific parameters and requirements.

