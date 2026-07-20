# xAI: Get Video Generation Model

Retrieves a video generation model from the xAI API.

```
GET https://connect.mindcloud.co/v1/universal/xAI/latest/actions/get-video-generation-model
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a xAI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/xAI/latest/actions/get-video-generation-model?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/xAI/latest/actions/get-video-generation-model?${params}`, {
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
| `model_id` | string | no | ID of the video generation model to retrieve. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": "string",
      "input_modalities": [
        "string"
      ],
      "object": "string",
      "output_modalities": [
        "string"
      ],
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
| `input_modalities` | array<string> |  |
| `object` | string |  |
| `output_modalities` | array<string> |  |
| `owned_by` | string |  |

## Native endpoint

Through the native xAI API, this operation is `GET /video-generation-models/:model_id` (base URL `https://api.x.ai/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-video-generation-model.md) for the provider-specific parameters and requirements.

