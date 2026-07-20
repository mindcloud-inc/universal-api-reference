# Dreamstudio: Generate Image from Image (Legacy)

Creates a legacy image-to-image result in Dreamstudio.

```
POST https://connect.mindcloud.co/v1/universal/dreamstudio/latest/actions/generate-image-from-image-legacy
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Dreamstudio `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/dreamstudio/latest/actions/generate-image-from-image-legacy" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "engineId": "string",
  "initImage": "string",
  "promptText": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/dreamstudio/latest/actions/generate-image-from-image-legacy', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "engineId": "string",
    "initImage": "string",
    "promptText": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `engineId` | string | yes | DreamStudio engine identifier for the legacy text-to-image endpoint. |
| `initImage` | file | yes | Starting image file for the legacy image-to-image request. |
| `promptText` | string<object> | yes | Prompt text for the legacy image-to-image request. |
| `initImageMode` | string | no | Use IMAGE_STRENGTH or STEP_SCHEDULE to control how strongly the init image is preserved. Default: `IMAGE_STRENGTH`. |
| `imageStrength` | number | no | How much the init image influences the output when init image mode is IMAGE_STRENGTH. Default: `0.35`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Dreamstudio API returns.

## Native endpoint

Through the native Dreamstudio API, this operation is `POST /v1/generation/:engine_id/image-to-image` (base URL `https://api.stability.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/generate-image-from-image-legacy.md) for the provider-specific parameters and requirements.

