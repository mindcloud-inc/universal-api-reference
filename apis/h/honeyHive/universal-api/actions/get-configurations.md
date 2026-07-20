# HoneyHive: Get Configurations

Retrieves a list of configurations from HoneyHive.

```
GET https://connect.mindcloud.co/v1/universal/honeyHive/latest/actions/get-configurations
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a HoneyHive `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/honeyHive/latest/actions/get-configurations?connectionId=$CONNECTION_ID&project=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "project": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/honeyHive/latest/actions/get-configurations?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as query string parameters ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `project` | string | yes | Project name for configuration. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "env": [
        "string"
      ],
      "id": "string",
      "name": "Ava Chen",
      "parameters": {
        "callType": "string",
        "forceFunction": {},
        "functionCallParams": "string",
        "hyperparameters": {},
        "model": "string",
        "responseFormat": {},
        "selectedFunctions": [
          {}
        ]
      },
      "project": "string",
      "provider": "string",
      "type": "string",
      "userProperties": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `env` | array<string> |  |
| `id` | string |  |
| `name` | string |  |
| `parameters` | object |  |
| `parameters.callType` | string |  |
| `parameters.forceFunction` | object |  |
| `parameters.functionCallParams` | string |  |
| `parameters.hyperparameters` | object |  |
| `parameters.model` | string |  |
| `parameters.responseFormat` | object |  |
| `parameters.selectedFunctions` | array<object> |  |
| `project` | string |  |
| `provider` | string |  |
| `type` | string |  |
| `userProperties` | object |  |

## Native endpoint

Through the native HoneyHive API, this operation is `GET /configurations` (base URL `https://api.honeyhive.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-configurations.md) for the provider-specific parameters and requirements.

