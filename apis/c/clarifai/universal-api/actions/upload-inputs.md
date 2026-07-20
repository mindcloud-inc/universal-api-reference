# Clarifai: Upload Inputs

Uploads inputs to an app in Clarifai.

```
POST https://connect.mindcloud.co/v1/universal/clarifai/latest/actions/upload-inputs
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Clarifai `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/clarifai/latest/actions/upload-inputs" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "appId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/clarifai/latest/actions/upload-inputs', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "appId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `appId` | string | yes | Clarifai app ID. |
| `inputs[]` | array<object> | no | Inputs to upload. |
| `inputs[].id` | string | no | Input ID. |
| `inputs[].data` | object | no | Input data. |
| `inputs[].data.image` | object | no | Image payload. |
| `inputs[].data.image.url` | string | no | Image URL to upload. |
| `inputs[].data.concepts[]` | array<object> | no | Concept annotations. |
| `inputs[].data.image.base64` | string | no | Base64-encoded image bytes. |
| `inputs[].data.concepts[].id` | string | no | Concept ID. |
| `inputs[].data.concepts[].value` | number | no | Concept score or label value. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Clarifai API returns.

## Native endpoint

Through the native Clarifai API, this operation is `POST /v2/users/me/apps/:appId/inputs` (base URL `https://api.clarifai.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/upload-inputs.md) for the provider-specific parameters and requirements.

