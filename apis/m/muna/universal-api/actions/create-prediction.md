# Muna: Create Prediction

Creates a prediction in Muna for a predictor tag.

```
POST https://connect.mindcloud.co/v1/universal/muna/latest/actions/create-prediction
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Muna `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/muna/latest/actions/create-prediction" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "tag": "my-predictor",
  "clientId": "client_123"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/muna/latest/actions/create-prediction', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "tag": "my-predictor",
    "clientId": "client_123"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `tag` | string | yes | Predictor tag. Example: `my-predictor`. |
| `clientId` | string | yes | Prediction client identifier. Example: `client_123`. |
| `configurationId` | string | no | Prediction configuration identifier. Example: `config_123`. |
| `deviceId` | string | no | Device identifier, used for choosing optimal implementation to respond with. Example: `device_123`. |
| `predictionId` | string | no | Original prediction identifier for embedded predictors. Example: `pred_123`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "configuration": "string",
      "created": "2026-05-07T12:00:00.000Z",
      "id": "string",
      "resources": {
        "name": "Ava Chen",
        "type": "string",
        "url": "https://example.com"
      },
      "tag": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `configuration` | string |  |
| `created` | date |  |
| `id` | string |  |
| `resources` | array<object> |  |
| `resources.name` | string |  |
| `resources.type` | string |  |
| `resources.url` | string |  |
| `tag` | string |  |

## Native endpoint

Through the native Muna API, this operation is `POST /v1/predictions` (base URL `https://api.muna.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-prediction.md) for the provider-specific parameters and requirements.

