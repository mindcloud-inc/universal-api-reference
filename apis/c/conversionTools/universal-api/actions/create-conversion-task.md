# Conversion Tools: Create Conversion Task

Creates a new conversion task in Conversion Tools.

```
POST https://connect.mindcloud.co/v1/universal/conversionTools/latest/actions/create-conversion-task
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Conversion Tools `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/conversionTools/latest/actions/create-conversion-task" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "type": "convert.jpg_to_pdf",
  "options": "[object Object]"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/conversionTools/latest/actions/create-conversion-task', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "type": "convert.jpg_to_pdf",
    "options": "[object Object]"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `type` | string | yes | Conversion type identifier from Conversion Tools, for example `convert.jpg_to_pdf` or `convert.xml_to_excel`. Example: `convert.jpg_to_pdf`. |
| `options` | object | yes | Task options object. Include the required conversion inputs such as `file_id` or `url`, plus any conversion-specific settings. Set `sandbox` to `true` for a free provider-side test run. Example: `[object Object]`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `callbackUrl` | string | no | Optional HTTPS endpoint that Conversion Tools should call when the task completes. Example: `https://example.com/webhooks/conversion-tools`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "error": "string",
      "message": "string",
      "sandbox": true,
      "task_id": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `error` | string | Provider error message when present. |
| `message` | string | Provider task-creation status message. |
| `sandbox` | boolean | Whether the task was created in sandbox mode. |
| `task_id` | string | Created conversion task ID. |

## Native endpoint

Through the native Conversion Tools API, this operation is `POST /tasks` (base URL `https://api.conversiontools.io/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-conversion-task.md) for the provider-specific parameters and requirements.

