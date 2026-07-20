# Rosette Text Analytics: Generate Semantic Vector



```
GET https://connect.mindcloud.co/v1/universal/rosetteTextAnalytics/latest/actions/generate-semantic-vector
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Rosette Text Analytics `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/rosetteTextAnalytics/latest/actions/generate-semantic-vector?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/rosetteTextAnalytics/latest/actions/generate-semantic-vector?${params}`, {
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
| `content` | string | no | Text to process. |
| `contentUri` | string | no | URI to accessible content. Mutually exclusive with content. |
| `language` | string | no | Three-letter ISO 639-3 language code. |
| `options.perToken` | boolean | no | If true, return a vector for each individual token. |
| `options.embeddingsMode` | string | no | Embeddings generation mode, such as GEN_1 or GEN_2. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "documentEmbedding": [
        1
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `documentEmbedding` | array<number> |  |

## Native endpoint

Through the native Rosette Text Analytics API, this operation is `POST /semantics/vector` (base URL `https://api.rosette.com/rest/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/generate-semantic-vector.md) for the provider-specific parameters and requirements.

