# Browse AI: Start Bulk Run

Starts a bulk run in Browse AI.

```
POST https://connect.mindcloud.co/v1/universal/browseAI/latest/actions/start-bulk-run
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Browse AI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/browseAI/latest/actions/start-bulk-run" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "robotId": "c3689adb-50aa-44af-b265-a7e0d4e5846e",
  "inputParameters[]": "[object Object],[object Object]"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/browseAI/latest/actions/start-bulk-run', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "robotId": "c3689adb-50aa-44af-b265-a7e0d4e5846e",
    "inputParameters[]": "[object Object],[object Object]",
    "inputParameters[]": "[object Object],[object Object]"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `robotId` | string | yes | Unique robot ID You can find a robot's ID by opening it on the dashboard and copying its ID in the browser address bar. Example: `c3689adb-50aa-44af-b265-a7e0d4e5846e`. |
| `title` | string | no | A string that describes the bulk run. Example: `Bulk Run Title`. |
| `inputParameters[]` | array<object> | yes | An array of input parameters to override the task's default input parameters. Example: `[object Object],[object Object]`. |
| `inputParameters[]` | array<object> | yes | An array of input parameters to override the task's default input parameters. Example: `[object Object],[object Object]`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "bulkRun": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `bulkRun` | object |  |

## Native endpoint

Through the native Browse AI API, this operation is `POST /robots/:robotId/bulk-runs` (base URL `https://api.browse.ai/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/start-bulk-run.md) for the provider-specific parameters and requirements.

