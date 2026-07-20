# Gemini: Async Batch Embed Content

Enqueues a batch embed content job in Gemini.

```
POST https://connect.mindcloud.co/v1/universal/gemini/latest/actions/async-batch-embed-content
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Gemini `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/gemini/latest/actions/async-batch-embed-content" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "model": "gemini-embedding-001:asyncBatchEmbedContent",
  "batch": "[object Object]"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/gemini/latest/actions/async-batch-embed-content', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "model": "gemini-embedding-001:asyncBatchEmbedContent",
    "batch": "[object Object]"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `model` | string | yes | Required. Model endpoint token including suffix, for example gemini-embedding-001:asyncBatchEmbedContent. Example: `gemini-embedding-001:asyncBatchEmbedContent`. |
| `batch` | object | yes | Required embed batch payload. Example: `[object Object]`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "metadata": {},
      "name": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `metadata` | object | Operation metadata including batch state and stats. |
| `name` | string | Long-running operation resource name. |

## Native endpoint

Through the native Gemini API, this operation is `POST v1beta/models/:model` (base URL `https://generativelanguage.googleapis.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/async-batch-embed-content.md) for the provider-specific parameters and requirements.

