# Stable Diffusion: Get Generation Result

Retrieves a generation result from Stable Diffusion.

```
GET https://connect.mindcloud.co/v1/universal/stableDiffusion/latest/actions/get-generation-result
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Stable Diffusion `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/stableDiffusion/latest/actions/get-generation-result?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/stableDiffusion/latest/actions/get-generation-result?${params}`, {
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
| `id` | string | yes | Generation identifier returned by an asynchronous Stability endpoint. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "finish_reason": "string",
      "id": "string",
      "image": "string",
      "seed": 1,
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `finish_reason` | string |  |
| `id` | string |  |
| `image` | string |  |
| `seed` | number |  |
| `status` | string |  |

## Native endpoint

Through the native Stable Diffusion API, this operation is `GET /v2beta/results/{id}` (base URL `https://api.stability.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-generation-result.md) for the provider-specific parameters and requirements.

