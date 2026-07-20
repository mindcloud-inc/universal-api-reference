# xAI: Get Image Generation Model

Retrieves an image generation model from the xAI API.

```
GET https://connect.mindcloud.co/v1/universal/xAI/latest/actions/get-image-generation-model
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a xAI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/xAI/latest/actions/get-image-generation-model?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/xAI/latest/actions/get-image-generation-model?${params}`, {
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
| `model_id` | string | no | ID of the image generation model to retrieve. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": "string",
      "max_prompt_length": 1,
      "object": "string",
      "owned_by": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | string |  |
| `max_prompt_length` | number |  |
| `object` | string |  |
| `owned_by` | string |  |

## Native endpoint

Through the native xAI API, this operation is `GET /image-generation-models/:model_id` (base URL `https://api.x.ai/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-image-generation-model.md) for the provider-specific parameters and requirements.

