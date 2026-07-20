# Cerebras AI: Retrieve Public Model (Generic Format)

Retrieves a public model from Cerebras AI by format.

```
GET https://connect.mindcloud.co/v1/universal/cerebrasAI/latest/actions/retrieve-public-model-by-format
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Cerebras AI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/cerebrasAI/latest/actions/retrieve-public-model-by-format?connectionId=$CONNECTION_ID&modelId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "modelId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/cerebrasAI/latest/actions/retrieve-public-model-by-format?${params}`, {
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
| `modelId` | string | yes |  |
| `format` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "created": 1,
      "description": "string",
      "id": "string",
      "name": "Ava Chen",
      "pricing": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `created` | number |  |
| `description` | string |  |
| `id` | string |  |
| `name` | string |  |
| `pricing` | object |  |

## Native endpoint

Through the native Cerebras AI API, this operation is `GET /public/v1/models/:modelId` (base URL `https://api.cerebras.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/retrieve-public-model-by-format.md) for the provider-specific parameters and requirements.

