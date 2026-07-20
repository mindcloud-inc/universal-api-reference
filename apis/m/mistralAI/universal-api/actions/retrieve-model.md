# Mistral AI: Retrieve Model

Retrieves model details from Mistral AI.

```
GET https://connect.mindcloud.co/v1/universal/mistralAI/latest/actions/retrieve-model
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Mistral AI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/mistralAI/latest/actions/retrieve-model?connectionId=$CONNECTION_ID&modelId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "modelId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/mistralAI/latest/actions/retrieve-model?${params}`, {
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
| `modelId` | string | yes | The ID of the model to retrieve. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "aliases": [
        "string"
      ],
      "capabilities": {},
      "created": 1,
      "default_model_temperature": 1,
      "deprecation": "string",
      "deprecation_replacement_model": "string",
      "description": "string",
      "id": "string",
      "max_context_length": 1,
      "name": "Ava Chen",
      "object": "string",
      "owned_by": "string",
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `aliases` | array<string> |  |
| `capabilities` | object |  |
| `created` | number |  |
| `default_model_temperature` | number |  |
| `deprecation` | string |  |
| `deprecation_replacement_model` | string |  |
| `description` | string |  |
| `id` | string |  |
| `max_context_length` | number |  |
| `name` | string |  |
| `object` | string |  |
| `owned_by` | string |  |
| `type` | string |  |

## Native endpoint

Through the native Mistral AI API, this operation is `GET /v1/models/:model_id` (base URL `https://api.mistral.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/retrieve-model.md) for the provider-specific parameters and requirements.

