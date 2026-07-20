# NextBrain: Train Model

Starts training a model in NextBrain.

```
PUT https://connect.mindcloud.co/v1/universal/nextBrain/latest/actions/train-model
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a NextBrain `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/nextBrain/latest/actions/train-model" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "modelId": "string",
  "target": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/nextBrain/latest/actions/train-model', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "modelId": "string",
    "target": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `modelId` | string | yes | The NextBrain model ID to train. |
| `target` | string | yes | The target column to train against. |
| `isLightning` | boolean | no | Whether to request Lightning training mode. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native NextBrain API returns.

## Native endpoint

Through the native NextBrain API, this operation is `POST /model/train_token` (base URL `https://api.nextbrain.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/train-model.md) for the provider-specific parameters and requirements.

