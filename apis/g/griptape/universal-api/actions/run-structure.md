# Griptape: Run Structure

Runs a structure in Griptape.

```
POST https://connect.mindcloud.co/v1/universal/griptape/latest/actions/run-structure
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Griptape `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/griptape/latest/actions/run-structure" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "structureId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/griptape/latest/actions/run-structure', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "structureId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `structureId` | string | yes | The Griptape structure ID to run. |
| `args[]` | array | no | Optional positional arguments passed into the Structure Run. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `env_vars[]` | array<object> | no | Optional environment variables to inject into the Structure Run request. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "args": [
        "string"
      ],
      "completed_at": "string",
      "created_at": "string",
      "created_by": "string",
      "deployment_id": "string",
      "env_vars": [
        "string"
      ],
      "output": {},
      "output_timestamp": 1,
      "started_at": "string",
      "status": "string",
      "status_detail": "string",
      "structure_id": "string",
      "structure_run_id": "string",
      "updated_at": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `args` | array |  |
| `completed_at` | string |  |
| `created_at` | string |  |
| `created_by` | string |  |
| `deployment_id` | string |  |
| `env_vars` | array |  |
| `output` | object |  |
| `output_timestamp` | number |  |
| `started_at` | string |  |
| `status` | string |  |
| `status_detail` | string |  |
| `structure_id` | string |  |
| `structure_run_id` | string |  |
| `updated_at` | string |  |

## Native endpoint

Through the native Griptape API, this operation is `POST /api/structures/:structure_id/runs` (base URL `https://cloud.griptape.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/run-structure.md) for the provider-specific parameters and requirements.

