# Middesk: Create an agent run

Creates an agent run in Middesk.

```
POST https://connect.mindcloud.co/v1/universal/middesk/latest/actions/create-agent-run
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Middesk `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/middesk/latest/actions/create-agent-run" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "type": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/middesk/latest/actions/create-agent-run', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "type": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `type` | string | yes | Type of agent run to create. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdAt": "string",
      "endedAt": "string",
      "id": "string",
      "interrupts": [
        {}
      ],
      "object": "string",
      "startedAt": "string",
      "status": "string",
      "steps": [
        {}
      ],
      "updatedAt": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdAt` | string |  |
| `endedAt` | string |  |
| `id` | string |  |
| `interrupts` | array<object> |  |
| `object` | string |  |
| `startedAt` | string |  |
| `status` | string |  |
| `steps` | array<object> |  |
| `updatedAt` | string |  |

## Native endpoint

Through the native Middesk API, this operation is `POST /runs` (base URL `https://api.middesk.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-agent-run.md) for the provider-specific parameters and requirements.

