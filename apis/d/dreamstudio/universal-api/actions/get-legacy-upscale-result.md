# Dreamstudio: Get Legacy Upscale Result

Retrieves a legacy upscale result from Dreamstudio.

```
GET https://connect.mindcloud.co/v1/universal/dreamstudio/latest/actions/get-legacy-upscale-result
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Dreamstudio `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/dreamstudio/latest/actions/get-legacy-upscale-result?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/dreamstudio/latest/actions/get-legacy-upscale-result?${params}`, {
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
| `id` | string | yes | Async upscale job identifier. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Dreamstudio API returns.

## Native endpoint

Through the native Dreamstudio API, this operation is `GET /v2alpha/generation/stable-image/upscale/result/:id` (base URL `https://api.stability.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-legacy-upscale-result.md) for the provider-specific parameters and requirements.

