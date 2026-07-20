# Cerebras AI: Upload Model Version

Creates a model version in Cerebras AI.

```
POST https://connect.mindcloud.co/v1/universal/cerebrasAI/latest/actions/upload-model-version
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Cerebras AI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/cerebrasAI/latest/actions/upload-model-version" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "orgName": "Ava Chen",
  "modelArchId": "string",
  "modelWeightUri": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/cerebrasAI/latest/actions/upload-model-version', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "orgName": "Ava Chen",
    "modelArchId": "string",
    "modelWeightUri": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `orgName` | string | yes |  |
| `modelArchId` | string | yes |  |
| `modelWeightUri` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "done": true,
      "name": "Ava Chen",
      "response": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `done` | boolean |  |
| `name` | string |  |
| `response` | object |  |

## Native endpoint

Through the native Cerebras AI API, this operation is `POST /management/v1/orgs/:orgName/models:upload` (base URL `https://api.cerebras.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/upload-model-version.md) for the provider-specific parameters and requirements.

