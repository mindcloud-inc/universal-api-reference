# Vectorizer AI: Vectorize



```
POST https://connect.mindcloud.co/v1/universal/vectorizerAI/latest/actions/vectorize
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Vectorizer AI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/vectorizerAI/latest/actions/vectorize" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/vectorizerAI/latest/actions/vectorize', {
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

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `image` | file | no |  |
| `mode` | list | no | One of: `preview`, `production`, `test`, `test_preview`. Default: `production`. |
| `input.max_pixels` | number | no | Default: `2097252`. |
| `processing.max_colors` | number | no | Default: `0`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `processing.palette` | string | no |  |
| `policy.retention_days` | number | no | Default: `0`. |
| `image.url` | string | no |  |
| `image.base64` | string | no |  |
| `image.token` | string | no |  |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Vectorizer AI API returns.

## Native endpoint

Through the native Vectorizer AI API, this operation is `POST /vectorize` (base URL `https://api.vectorizer.ai/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/vectorize.md) for the provider-specific parameters and requirements.

