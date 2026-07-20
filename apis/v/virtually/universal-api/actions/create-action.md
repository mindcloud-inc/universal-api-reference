# Virtually: Create Action

Creates a new action in Virtually.

```
POST https://connect.mindcloud.co/v1/universal/virtually/latest/actions/create-action
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Virtually `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/virtually/latest/actions/create-action" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "message": {},
  "message.subject": "string",
  "message.content": "string",
  "channel": {},
  "channel.type": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/virtually/latest/actions/create-action', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "message": {},
    "message.subject": "string",
    "message.content": "string",
    "channel": {},
    "channel.type": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `name` | string | no |  |
| `description` | string | no |  |
| `message` | object | yes |  |
| `message.subject` | string | yes |  |
| `message.content` | string | yes |  |
| `channel` | object | yes |  |
| `channel.type` | string | yes |  |
| `channel.id` | string | no |  |
| `channel.sendAs` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "actionId": "string",
      "channel": {},
      "description": "string",
      "message": {},
      "name": "Ava Chen",
      "orgId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `actionId` | string |  |
| `channel` | object |  |
| `description` | string |  |
| `message` | object |  |
| `name` | string |  |
| `orgId` | string |  |

## Native endpoint

Through the native Virtually API, this operation is `POST /api/v2/orgs/:orgId/actions` (base URL `https://app.tryvirtually.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-action.md) for the provider-specific parameters and requirements.

