# Virtually: Update Action

Updates an existing action in Virtually.

```
PUT https://connect.mindcloud.co/v1/universal/virtually/latest/actions/update-action
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Virtually `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/virtually/latest/actions/update-action" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "actionId": "string",
  "message": {},
  "message.subject": "string",
  "message.content": "string",
  "channel": {},
  "channel.type": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/virtually/latest/actions/update-action', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "actionId": "string",
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
| `actionId` | string | yes |  |
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

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Virtually API returns.

## Native endpoint

Through the native Virtually API, this operation is `PATCH /api/v2/orgs/:orgId/actions/:actionId` (base URL `https://app.tryvirtually.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-action.md) for the provider-specific parameters and requirements.

