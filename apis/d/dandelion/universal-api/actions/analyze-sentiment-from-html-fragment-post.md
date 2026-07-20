# Dandelion: Analyze Sentiment From HTML Fragment via HTTP POST

Retrieves sentiment from an HTML fragment in Dandelion via HTTP POST.

```
GET https://connect.mindcloud.co/v1/universal/dandelion/latest/actions/analyze-sentiment-from-html-fragment-post
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Dandelion `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/dandelion/latest/actions/analyze-sentiment-from-html-fragment-post?connectionId=$CONNECTION_ID&htmlFragment=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "htmlFragment": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/dandelion/latest/actions/analyze-sentiment-from-html-fragment-post?${params}`, {
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
| `htmlFragment` | string | yes | HTML Fragment to analyze. |
| `lang` | string | no | Language code to force sentiment analysis language. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "lang": "string",
      "langConfidence": 1,
      "sentiment": {},
      "time": 1,
      "timestamp": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `lang` | string |  |
| `langConfidence` | number |  |
| `sentiment` | object |  |
| `time` | number |  |
| `timestamp` | string |  |

## Native endpoint

Through the native Dandelion API, this operation is `POST /datatxt/sent/v1` (base URL `https://api.dandelion.eu`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/analyze-sentiment-from-html-fragment-post.md) for the provider-specific parameters and requirements.

