# Scale: Create Chat Task



```
POST https://connect.mindcloud.co/v1/universal/scale/latest/actions/create-chat-task
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Scale `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/scale/latest/actions/create-chat-task" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "templateVariables": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/scale/latest/actions/create-chat-task', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "templateVariables": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `templateVariables` | string | yes | Template variables supplied to the chat task. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": "string",
      "metadata": {},
      "project_name": "Ava Chen",
      "template_variables": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | string |  |
| `metadata` | object |  |
| `project_name` | string |  |
| `template_variables` | object |  |

## Native endpoint

Through the native Scale API, this operation is `POST /v2/task/chat` (base URL `https://api.scale.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-chat-task.md) for the provider-specific parameters and requirements.

