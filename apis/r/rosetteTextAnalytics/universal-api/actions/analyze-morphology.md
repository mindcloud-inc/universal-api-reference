# Rosette Text Analytics: Analyze Morphology



```
GET https://connect.mindcloud.co/v1/universal/rosetteTextAnalytics/latest/actions/analyze-morphology
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Rosette Text Analytics `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/rosetteTextAnalytics/latest/actions/analyze-morphology?connectionId=$CONNECTION_ID&morphoFeature=complete" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "morphoFeature": "complete"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/rosetteTextAnalytics/latest/actions/analyze-morphology?${params}`, {
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
| `morphoFeature` | string | yes | Morphology feature path segment. Use complete for all supported morphology features. Default: `complete`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "compoundComponents": [
        "string"
      ],
      "hanReadings": [
        "string"
      ],
      "lemmas": [
        "string"
      ],
      "posTags": [
        "string"
      ],
      "tokens": [
        "string"
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `compoundComponents` | array<string> |  |
| `hanReadings` | array<string> |  |
| `lemmas` | array<string> |  |
| `posTags` | array<string> |  |
| `tokens` | array<string> |  |

## Native endpoint

Through the native Rosette Text Analytics API, this operation is `POST /morphology/:morphoFeature` (base URL `https://api.rosette.com/rest/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/analyze-morphology.md) for the provider-specific parameters and requirements.

