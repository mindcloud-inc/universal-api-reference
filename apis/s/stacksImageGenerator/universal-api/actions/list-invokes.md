# 88stacks Image Generator: List Invokes

Retrieves image generation requests for a model in 88stacks Image Generator.

```
GET https://connect.mindcloud.co/v1/universal/stacksImageGenerator/latest/actions/list-invokes
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a 88stacks Image Generator `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/stacksImageGenerator/latest/actions/list-invokes?connectionId=$CONNECTION_ID&modelId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "modelId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/stacksImageGenerator/latest/actions/list-invokes?${params}`, {
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
| `modelId` | string | yes | Model ID whose invokes you want to list. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "prompt": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `prompt` | string | Prompt text for an invoke item. Inferred conservatively from the official docs description that this endpoint returns a list of prompts for a model. |

## Native endpoint

Through the native 88stacks Image Generator API, this operation is `GET /api/v1/invokes` (base URL `https://api.88stacks.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-invokes.md) for the provider-specific parameters and requirements.

