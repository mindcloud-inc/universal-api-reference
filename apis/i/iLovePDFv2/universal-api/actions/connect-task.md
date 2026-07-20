# iLovePDFv2: Connect Task

Creates a follow-up task from an iLovePDFv2 task.

```
POST https://connect.mindcloud.co/v1/universal/iLovePDFv2/latest/actions/connect-task
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a iLovePDFv2 `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/iLovePDFv2/latest/actions/connect-task" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "server": "string",
  "task": "string",
  "tool": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/iLovePDFv2/latest/actions/connect-task', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "server": "string",
    "task": "string",
    "tool": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `server` | string | yes | Processing server from parent task. |
| `task` | string | yes | Parent task ID. |
| `tool` | string | yes | Next tool to run. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "files": [
        {}
      ],
      "task": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `files` | array<object> |  |
| `task` | string |  |

## Native endpoint

Through the native iLovePDFv2 API, this operation is `POST https://:server/v1/task/next` (base URL `https://api.ilovepdf.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/connect-task.md) for the provider-specific parameters and requirements.

