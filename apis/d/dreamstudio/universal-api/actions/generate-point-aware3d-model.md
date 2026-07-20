# Dreamstudio: Generate Point-Aware 3D Model

Creates a point-aware 3D model in Dreamstudio.

```
POST https://connect.mindcloud.co/v1/universal/dreamstudio/latest/actions/generate-point-aware3d-model
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Dreamstudio `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/dreamstudio/latest/actions/generate-point-aware3d-model" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "image": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/dreamstudio/latest/actions/generate-point-aware3d-model', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "image": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `image` | file | yes | Single image file used to generate a point-aware 3D model. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Dreamstudio API returns.

## Native endpoint

Through the native Dreamstudio API, this operation is `POST /v2beta/3d/stable-point-aware-3d` (base URL `https://api.stability.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/generate-point-aware3d-model.md) for the provider-specific parameters and requirements.

