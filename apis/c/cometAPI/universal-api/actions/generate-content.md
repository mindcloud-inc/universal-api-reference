# CometAPI: Generate Content

Generates content with Gemini models in CometAPI.

```
POST https://connect.mindcloud.co/v1/universal/cometAPI/latest/actions/generate-content
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a CometAPI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/cometAPI/latest/actions/generate-content" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "contents[]": [
    {}
  ],
  "model": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/cometAPI/latest/actions/generate-content', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "contents[]": [{}],
    "model": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `contents[]` | array<object> | yes | Gemini contents array. |
| `model` | string | yes | Gemini model ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "candidates": [
        {}
      ],
      "modelVersion": "string",
      "responseId": "string",
      "usageMetadata": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `candidates` | array<object> |  |
| `modelVersion` | string |  |
| `responseId` | string |  |
| `usageMetadata` | object |  |

## Native endpoint

Through the native CometAPI API, this operation is `POST /v1beta/models/:model` (base URL `https://api.cometapi.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/generate-content.md) for the provider-specific parameters and requirements.

