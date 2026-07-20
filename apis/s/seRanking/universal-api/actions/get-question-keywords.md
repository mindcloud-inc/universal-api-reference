# SE Ranking Data: Get question keywords

Retrieves question keywords from SE Ranking Data.

```
GET https://connect.mindcloud.co/v1/universal/seRanking/latest/actions/get-question-keywords
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SE Ranking Data `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/seRanking/latest/actions/get-question-keywords?connectionId=$CONNECTION_ID&keyword=seo%20tools&source=us" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "keyword": "seo tools",
  "source": "us"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/seRanking/latest/actions/get-question-keywords?${params}`, {
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
| `keyword` | string | yes | Keyword phrase (for example: seo tools). Example: `seo tools`. |
| `source` | string | yes | Regional database code (for example: us). Example: `us`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "keywords": [
        {
          "competition": 1,
          "cpc": 1,
          "difficulty": 1,
          "intents": [
            "string"
          ],
          "keyword": "string",
          "serpFeatures": [
            "string"
          ],
          "volume": 1
        }
      ],
      "total": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `keywords` | array<object> | Question keyword rows with metrics. |
| `keywords[].competition` | number |  |
| `keywords[].cpc` | number |  |
| `keywords[].difficulty` | number |  |
| `keywords[].intents` | array<string> |  |
| `keywords[].keyword` | string |  |
| `keywords[].serpFeatures` | array<string> |  |
| `keywords[].volume` | number |  |
| `total` | number | Total question keywords available. |

## Native endpoint

Through the native SE Ranking Data API, this operation is `GET /keywords/questions` (base URL `https://api.seranking.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-question-keywords.md) for the provider-specific parameters and requirements.

