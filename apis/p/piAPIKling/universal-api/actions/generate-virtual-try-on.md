# PiAPI/Kling: Generate Virtual Try-On



```
POST https://connect.mindcloud.co/v1/universal/piAPIKling/latest/actions/generate-virtual-try-on
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a PiAPI/Kling `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/piAPIKling/latest/actions/generate-virtual-try-on" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "input.modelInput": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/piAPIKling/latest/actions/generate-virtual-try-on', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "input.modelInput": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `input.modelInput` | string | yes | Model or person image URL for the try-on request. |
| `input.upperInput` | string | no | Upper garment image URL. |
| `input.lowerInput` | string | no | Lower garment image URL. |
| `input.batchSize` | number | no | Number of try-on outputs to generate. PiAPI accepts values from 1 to 4. Default: `1`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "config": {},
      "detail": {},
      "error": {},
      "input": {},
      "logs": [
        {}
      ],
      "meta": {},
      "model": "string",
      "output": {},
      "status": "string",
      "taskId": "string",
      "taskType": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `config` | object | Resolved task configuration. |
| `detail` | object | Provider detail payload when available. |
| `error` | object | Provider error payload. |
| `input` | object | Submitted task input payload. |
| `logs` | array<object> | Task log entries when available. |
| `meta` | object | Task timestamps and usage metadata. |
| `model` | string | Provider model name. |
| `output` | object | Provider output payload. |
| `status` | string | Current task status. |
| `taskId` | string | PiAPI task identifier. |
| `taskType` | string | PiAPI task type. |

## Native endpoint

Through the native PiAPI/Kling API, this operation is `POST /api/v1/task` (base URL `https://api.piapi.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/generate-virtual-try-on.md) for the provider-specific parameters and requirements.

