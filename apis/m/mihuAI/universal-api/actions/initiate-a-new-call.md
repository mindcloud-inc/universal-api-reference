# Mihu AI: Initiate a New Call



```
POST https://connect.mindcloud.co/v1/universal/mihuAI/latest/actions/initiate-a-new-call
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Mihu AI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/mihuAI/latest/actions/initiate-a-new-call" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "agentId": "string",
  "participant.number": "string",
  "prompt.overwrite": true
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/mihuAI/latest/actions/initiate-a-new-call', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "agentId": "string",
    "participant.number": "string",
    "prompt.overwrite": true
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `agentId` | string | yes |  |
| `message.start` | string | no |  |
| `participant.about` | string | no |  |
| `participant.number` | string | yes |  |
| `prompt.content` | string | no |  |
| `prompt.overwrite` | boolean | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "agentId": "string",
      "id": "string",
      "provider": "string",
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `agentId` | string |  |
| `id` | string |  |
| `provider` | string |  |
| `status` | string |  |

## Native endpoint

Through the native Mihu AI API, this operation is `POST /api/v1/call` (base URL `https://{{credentials.subdomain}}.mindhunters.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/initiate-a-new-call.md) for the provider-specific parameters and requirements.

