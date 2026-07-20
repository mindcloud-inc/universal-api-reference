# EDEN AI: Moderate Text

Creates a text moderation request in EDEN AI.

```
POST https://connect.mindcloud.co/v1/universal/eDENAI/latest/actions/moderate-text
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a EDEN AI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/eDENAI/latest/actions/moderate-text" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/eDENAI/latest/actions/moderate-text', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "cost": "string",
      "error": {},
      "feature": "string",
      "originalResponse": {},
      "output": {
        "items": [
          {}
        ],
        "nsfwLikelihood": 1,
        "nsfwLikelihoodScore": 1
      },
      "provider": "string",
      "status": "string",
      "subfeature": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `cost` | string | Reported cost of the moderation request. |
| `error` | object | Provider error payload when present. |
| `feature` | string | Top-level feature category. |
| `originalResponse` | object | Original provider response when requested. |
| `output` | object | Moderation output payload. |
| `output.items` | array<object> | Detected moderation labels. |
| `output.nsfwLikelihood` | number | NSFW likelihood bucket. |
| `output.nsfwLikelihoodScore` | number | NSFW likelihood confidence score. |
| `provider` | string | Provider used to execute the moderation. |
| `status` | string | Execution status returned by Eden AI. |
| `subfeature` | string | Specific subfeature key. |

## Native endpoint

Through the native EDEN AI API, this operation is `POST /universal-ai` (base URL `https://api.edenai.run/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/moderate-text.md) for the provider-specific parameters and requirements.

