# PiAPI/Flux.1: Create Flux ControlNet LoRA Task

Creates a Flux ControlNet LoRA task in PiAPI/Flux.1.

```
POST https://connect.mindcloud.co/v1/universal/piAPIFlux1/latest/actions/create-flux-control-net-lo-ra-task
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a PiAPI/Flux.1 `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/piAPIFlux1/latest/actions/create-flux-control-net-lo-ra-task" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "input.prompt": "string",
  "input.controlNetSettings[]": [
    "string"
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/piAPIFlux1/latest/actions/create-flux-control-net-lo-ra-task', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "input.prompt": "string",
    "input.controlNetSettings[]": ["string"]
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `input.prompt` | string | yes |  |
| `input.controlNetSettings[]` | array | yes |  |
| `input.loraSettings[]` | array | no |  |
| `input.steps` | number | no |  |
| `input.negativePrompt` | string | no |  |
| `input.guidanceScale` | number | no |  |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `config.webhookConfig.endpoint` | string | no |  |
| `config.webhookConfig.secret` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "code": 1,
      "data": {
        "config": {
          "service_mode": "string",
          "webhook_config": {
            "endpoint": "string",
            "secret": "string"
          }
        },
        "error": {
          "code": 1,
          "message": "string",
          "raw_message": "string"
        },
        "input": {},
        "logs": [
          {}
        ],
        "meta": {
          "created_at": "string",
          "ended_at": "string",
          "is_using_private_pool": true,
          "started_at": "string",
          "usage": {
            "consume": 1,
            "frozen": 1,
            "type": "string"
          }
        },
        "model": "string",
        "output": {},
        "status": "string",
        "task_id": "string",
        "task_type": "string"
      },
      "message": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `code` | number |  |
| `data.config.service_mode` | string |  |
| `data.config.webhook_config.endpoint` | string |  |
| `data.config.webhook_config.secret` | string |  |
| `data.error.code` | number |  |
| `data.error.message` | string |  |
| `data.error.raw_message` | string |  |
| `data.input` | object |  |
| `data.logs` | array<object> |  |
| `data.meta.created_at` | string |  |
| `data.meta.ended_at` | string |  |
| `data.meta.is_using_private_pool` | boolean |  |
| `data.meta.started_at` | string |  |
| `data.meta.usage.consume` | number |  |
| `data.meta.usage.frozen` | number |  |
| `data.meta.usage.type` | string |  |
| `data.model` | string |  |
| `data.output` | object |  |
| `data.status` | string |  |
| `data.task_id` | string |  |
| `data.task_type` | string |  |
| `message` | string |  |

## Native endpoint

Through the native PiAPI/Flux.1 API, this operation is `POST /api/v1/task` (base URL `https://api.piapi.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-flux-control-net-lo-ra-task.md) for the provider-specific parameters and requirements.

