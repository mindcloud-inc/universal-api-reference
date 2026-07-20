# Manus: Create Task

Creates a new task in Manus.

```
POST https://connect.mindcloud.co/v1/universal/manus/latest/actions/create-task
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Manus `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/manus/latest/actions/create-task" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "prompt": "string",
  "agentProfile": "manus-1.6"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/manus/latest/actions/create-task', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "prompt": "string",
    "agentProfile": "manus-1.6"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `prompt` | string | yes | The task prompt or instruction for the Manus agent |
| `agentProfile` | string | yes | The Manus model profile to use Default: `manus-1.6`. |
| `taskMode` | string | no | Task mode: chat, adaptive, or agent |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `hideInTaskList` | boolean | no | Hide the task from the Manus web app task list |
| `createShareableLink` | boolean | no | Make the chat publicly accessible |
| `taskId` | string | no | Continue an existing task |
| `locale` | string | no | Locale such as en-US |
| `interactiveMode` | boolean | no | Allow Manus to ask follow-up questions |

## Response

```json
{
  "success": true,
  "data": [
    {
      "taskId": "string",
      "taskTitle": "string",
      "taskUrl": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `taskId` | string |  |
| `taskTitle` | string |  |
| `taskUrl` | string |  |

## Native endpoint

Through the native Manus API, this operation is `POST /tasks` (base URL `https://api.manus.ai/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-task.md) for the provider-specific parameters and requirements.

