# Dreamstudio: Stable Image Core

Creates an image with Stable Image Core in Dreamstudio.

```
POST https://connect.mindcloud.co/v1/universal/dreamstudio/latest/actions/stable-image-core
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Dreamstudio `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/dreamstudio/latest/actions/stable-image-core" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "prompt": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/dreamstudio/latest/actions/stable-image-core', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "prompt": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `prompt` | string | yes | Prompt used to generate the image. |
| `outputFormat` | string | no | Optional output file format for the generated image. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Dreamstudio API returns.

## Native endpoint

Through the native Dreamstudio API, this operation is `POST /v2beta/stable-image/generate/core` (base URL `https://api.stability.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/stable-image-core.md) for the provider-specific parameters and requirements.

