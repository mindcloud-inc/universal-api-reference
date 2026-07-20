# Mistral AI: Update Fine Tuned Model

Updates an existing fine-tuned model in Mistral AI.

```
PUT https://connect.mindcloud.co/v1/universal/mistralAI/latest/actions/update-fine-tuned-model
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Mistral AI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/mistralAI/latest/actions/update-fine-tuned-model" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "modelId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/mistralAI/latest/actions/update-fine-tuned-model', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "modelId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `modelId` | string | yes | The ID of the fine-tuned model. |
| `name` | string | no | Updated model name. |
| `description` | string | no | Updated model description. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "archived": true,
      "capabilities": {},
      "created": 1,
      "id": "string",
      "job": "string",
      "owned_by": "string",
      "root": "string",
      "root_version": "string",
      "workspace_id": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `archived` | boolean |  |
| `capabilities` | object |  |
| `created` | number |  |
| `id` | string |  |
| `job` | string |  |
| `owned_by` | string |  |
| `root` | string |  |
| `root_version` | string |  |
| `workspace_id` | string |  |

## Native endpoint

Through the native Mistral AI API, this operation is `PATCH /v1/fine_tuning/models/:model_id` (base URL `https://api.mistral.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-fine-tuned-model.md) for the provider-specific parameters and requirements.

