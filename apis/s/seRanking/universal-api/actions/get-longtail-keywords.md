# SE Ranking Data: Get longtail keywords

Retrieves longtail keywords from SE Ranking Data.

```
GET https://connect.mindcloud.co/v1/universal/seRanking/latest/actions/get-longtail-keywords
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SE Ranking Data `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/seRanking/latest/actions/get-longtail-keywords?connectionId=$CONNECTION_ID&keyword=seo%20tools&source=us" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "keyword": "seo tools",
  "source": "us"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/seRanking/latest/actions/get-longtail-keywords?${params}`, {
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
        "string"
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
| `keywords` | array<string> | Longtail keyword strings. |
| `total` | number | Total longtail keywords available. |

## Native endpoint

Through the native SE Ranking Data API, this operation is `GET /keywords/longtail` (base URL `https://api.seranking.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-longtail-keywords.md) for the provider-specific parameters and requirements.

