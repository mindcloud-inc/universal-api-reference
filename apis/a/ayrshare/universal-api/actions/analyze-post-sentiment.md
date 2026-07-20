# Ayrshare: Analyze Post Sentiment

Analyzes sentiment for a post or comment in Ayrshare.

```
GET https://connect.mindcloud.co/v1/universal/ayrshare/latest/actions/analyze-post-sentiment
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Ayrshare `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/ayrshare/latest/actions/analyze-post-sentiment?connectionId=$CONNECTION_ID&text=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "text": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/ayrshare/latest/actions/analyze-post-sentiment?${params}`, {
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
| `text` | string | yes | Text to analyze for sentiment. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "code": 1,
      "message": "string",
      "score": 1,
      "sentiment": "string",
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `code` | number | Ayrshare error code. |
| `message` | string | Sentiment or error message. |
| `score` | number | Sentiment score when returned. |
| `sentiment` | string | Detected sentiment label. |
| `status` | string | Sentiment request status. |

## Native endpoint

Through the native Ayrshare API, this operation is `POST /generate/sentiment` (base URL `https://api.ayrshare.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/analyze-post-sentiment.md) for the provider-specific parameters and requirements.

