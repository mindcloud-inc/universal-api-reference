# Sapling: Analyze Sentiment

Analyzes sentiment in text with Sapling.

```
GET https://connect.mindcloud.co/v1/universal/sapling/latest/actions/analyze-sentiment
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Sapling `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sapling/latest/actions/analyze-sentiment?connectionId=$CONNECTION_ID&text=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "text": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/sapling/latest/actions/analyze-sentiment?${params}`, {
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
| `text` | string | yes | Text to analyze the sentiment for. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "overall": [
        {}
      ],
      "results": [
        {}
      ],
      "sents": [
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
| `overall` | array<object> | Overall sentiment classification. |
| `results` | array<object> | Per-span sentiment analysis. |
| `sents` | array<string> | Normalized sentence list. |

## Native endpoint

Through the native Sapling API, this operation is `POST /api/v1/sentiment` (base URL `https://api.sapling.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/analyze-sentiment.md) for the provider-specific parameters and requirements.

