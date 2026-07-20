# CometAPI: Replicate Create Prediction

Creates a Replicate prediction in CometAPI.

```
POST https://connect.mindcloud.co/v1/universal/cometAPI/latest/actions/replicate-create-prediction
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a CometAPI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/cometAPI/latest/actions/replicate-create-prediction" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "input": {},
  "models": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/cometAPI/latest/actions/replicate-create-prediction', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "input": {},
    "models": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `input` | object | yes | Prediction input object. |
| `models` | string | yes | Replicate model path. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": "string",
      "output": {},
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | string |  |
| `output` | object |  |
| `status` | string |  |

## Native endpoint

Through the native CometAPI API, this operation is `POST /replicate/v1/models/:models/predictions` (base URL `https://api.cometapi.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/replicate-create-prediction.md) for the provider-specific parameters and requirements.

