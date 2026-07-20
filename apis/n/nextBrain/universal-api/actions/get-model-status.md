# NextBrain: Get Model Status

Retrieves a model status from NextBrain.

```
GET https://connect.mindcloud.co/v1/universal/nextBrain/latest/actions/get-model-status
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a NextBrain `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/nextBrain/latest/actions/get-model-status?connectionId=$CONNECTION_ID&modelId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "modelId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/nextBrain/latest/actions/get-model-status?${params}`, {
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
| `modelId` | string | yes | The NextBrain model ID. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native NextBrain API returns.

## Native endpoint

Through the native NextBrain API, this operation is `POST /model/status_token/:model_id` (base URL `https://api.nextbrain.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-model-status.md) for the provider-specific parameters and requirements.

