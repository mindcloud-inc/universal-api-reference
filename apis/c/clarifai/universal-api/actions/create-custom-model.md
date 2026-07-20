# Clarifai: Create Custom Model

Creates a custom model in Clarifai.

```
POST https://connect.mindcloud.co/v1/universal/clarifai/latest/actions/create-custom-model
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Clarifai `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/clarifai/latest/actions/create-custom-model" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "appId": "string",
  "model": {},
  "model.id": "string",
  "model.model_type_id": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/clarifai/latest/actions/create-custom-model', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "appId": "string",
    "model": {},
    "model.id": "string",
    "model.model_type_id": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `appId` | string | yes | Clarifai app ID. |
| `model` | object | yes | Model to create. |
| `model.id` | string | yes | Model ID. |
| `model.model_type_id` | string | yes | Clarifai model type ID. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Clarifai API returns.

## Native endpoint

Through the native Clarifai API, this operation is `POST /v2/users/me/apps/:appId/models` (base URL `https://api.clarifai.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-custom-model.md) for the provider-specific parameters and requirements.

