# iLovePDFv2: Process Task

Processes uploaded files for an iLovePDFv2 task.

```
POST https://connect.mindcloud.co/v1/universal/iLovePDFv2/latest/actions/process-task
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a iLovePDFv2 `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/iLovePDFv2/latest/actions/process-task" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "server": "string",
  "task": "string",
  "tool": "string",
  "files[]": [
    {}
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/iLovePDFv2/latest/actions/process-task', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "server": "string",
    "task": "string",
    "tool": "string",
    "files[]": [{}]
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `server` | string | yes | Processing server from Start Task. |
| `task` | string | yes | Task ID to process. |
| `tool` | string | yes | Tool used for this task. |
| `files[]` | array<object> | yes | Files array from upload results. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "download_filename": "Ava Chen",
      "output_filenumber": 1,
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `download_filename` | string |  |
| `output_filenumber` | number |  |
| `status` | string |  |

## Native endpoint

Through the native iLovePDFv2 API, this operation is `POST https://:server/v1/process` (base URL `https://api.ilovepdf.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/process-task.md) for the provider-specific parameters and requirements.

