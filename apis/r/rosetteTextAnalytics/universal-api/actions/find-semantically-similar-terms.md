# Rosette Text Analytics: Find Semantically Similar Terms



```
GET https://connect.mindcloud.co/v1/universal/rosetteTextAnalytics/latest/actions/find-semantically-similar-terms
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Rosette Text Analytics `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/rosetteTextAnalytics/latest/actions/find-semantically-similar-terms?connectionId=$CONNECTION_ID&content=string&options.resultLanguages%5B%5D=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "content": "string",
  "options.resultLanguages[]": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/rosetteTextAnalytics/latest/actions/find-semantically-similar-terms?${params}`, {
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
| `content` | string | yes | Input term or text to compare in semantic space. |
| `language` | string | no | Three-letter ISO 639-3 language code for the input. |
| `options.resultLanguages[]` | array<string> | yes | One or more three-letter language codes to return similar terms in. |
| `options.count` | number | no | Number of similar terms to return per result language, from 1 to 50. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "similarTerms": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `similarTerms` | object |  |

## Native endpoint

Through the native Rosette Text Analytics API, this operation is `POST /semantics/similar` (base URL `https://api.rosette.com/rest/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/find-semantically-similar-terms.md) for the provider-specific parameters and requirements.

