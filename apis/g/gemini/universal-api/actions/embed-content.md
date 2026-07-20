# Gemini: Embed Content

Generates content embeddings with Gemini.

```
POST https://connect.mindcloud.co/v1/universal/gemini/latest/actions/embed-content
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Gemini `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/gemini/latest/actions/embed-content" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "model": "gemini-embedding-001:embedContent",
  "content": "[object Object]"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/gemini/latest/actions/embed-content', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "model": "gemini-embedding-001:embedContent",
    "content": "[object Object]"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `model` | string | yes | Required. Model endpoint token including suffix, for example gemini-embedding-001:embedContent. Example: `gemini-embedding-001:embedContent`. |
| `content` | object | yes | Required content object to embed. Example: `[object Object]`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `taskType` | string | no | Optional embedding task type. Example: `RETRIEVAL_QUERY`. |
| `title` | string | no | Optional title used for retrieval document embeddings. Example: `Product documentation section`. |
| `outputDimensionality` | number | no | Optional reduced embedding dimension. Example: `768`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "embedding": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `embedding` | object | Embedding payload containing numeric vector values. |

## Native endpoint

Through the native Gemini API, this operation is `POST v1beta/models/:model` (base URL `https://generativelanguage.googleapis.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/embed-content.md) for the provider-specific parameters and requirements.

