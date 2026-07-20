# Gemini: Predict Long Running

Starts a long-running prediction in Gemini.

```
POST https://connect.mindcloud.co/v1/universal/gemini/latest/actions/predict-long-running
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Gemini `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/gemini/latest/actions/predict-long-running" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "model": "veo-3.0-generate-001:predictLongRunning",
  "instances[]": "[object Object]"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/gemini/latest/actions/predict-long-running', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "model": "veo-3.0-generate-001:predictLongRunning",
    "instances[]": "[object Object]"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `model` | string | yes | Required. Model endpoint token including suffix, for example veo-3.0-generate-001:predictLongRunning. Example: `veo-3.0-generate-001:predictLongRunning`. |
| `instances[]` | array<object> | yes | Required prediction instances array. Example: `[object Object]`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `parameters` | object | no | Optional prediction parameters object. Example: `[object Object]`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "name": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `name` | string | Prediction long-running operation resource name. |

## Native endpoint

Through the native Gemini API, this operation is `POST v1beta/models/:model` (base URL `https://generativelanguage.googleapis.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/predict-long-running.md) for the provider-specific parameters and requirements.

