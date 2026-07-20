# HelpCrunch: Create Agent Message

Creates an agent message in HelpCrunch.

```
POST https://connect.mindcloud.co/v1/universal/helpCrunch/latest/actions/create-agent-message
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a HelpCrunch `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/helpCrunch/latest/actions/create-agent-message" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "agent": 1,
  "chat": 1,
  "text": "string",
  "type": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/helpCrunch/latest/actions/create-agent-message', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "agent": 1,
    "chat": 1,
    "text": "string",
    "type": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `agent` | number | yes |  |
| `chat` | number | yes |  |
| `text` | string | yes |  |
| `type` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "agent": {},
      "broadcastType": "string",
      "chat": 1,
      "createdAt": "string",
      "edited": true,
      "from": "string",
      "id": 1,
      "read": true,
      "text": "string",
      "type": "string",
      "updatedAt": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `agent` | object |  |
| `broadcastType` | string |  |
| `chat` | number |  |
| `createdAt` | string |  |
| `edited` | boolean |  |
| `from` | string |  |
| `id` | number |  |
| `read` | boolean |  |
| `text` | string |  |
| `type` | string |  |
| `updatedAt` | string |  |

## Native endpoint

Through the native HelpCrunch API, this operation is `POST /messages` (base URL `https://api.helpcrunch.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-agent-message.md) for the provider-specific parameters and requirements.

