# SE Ranking Data: Get paid ads by keyword

Retrieves paid ads by keyword from SE Ranking Data.

```
GET https://connect.mindcloud.co/v1/universal/seRanking/latest/actions/get-paid-ads-by-keyword
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SE Ranking Data `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/seRanking/latest/actions/get-paid-ads-by-keyword?connectionId=$CONNECTION_ID&keyword=seo%20tools&source=us" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "keyword": "seo tools",
  "source": "us"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/seRanking/latest/actions/get-paid-ads-by-keyword?${params}`, {
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
| `keyword` | string | yes | Keyword to analyze paid ads for (for example: seo tools). Example: `seo tools`. |
| `source` | string | yes | Regional database code (for example: us). Example: `us`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "adsCount": 1,
      "domain": "string",
      "keywordsCount": 1,
      "priceSum": 1,
      "snippets": [
        {
          "position": 1,
          "snippetCount": 1,
          "snippetDescription": "string",
          "snippetDisplayUrl": "https://example.com",
          "snippetTitle": "string",
          "url": "https://example.com"
        }
      ],
      "trafficSum": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `adsCount` | number |  |
| `domain` | string |  |
| `keywordsCount` | number |  |
| `priceSum` | number |  |
| `snippets` | array<object> |  |
| `snippets[].position` | number |  |
| `snippets[].snippetCount` | number |  |
| `snippets[].snippetDescription` | string |  |
| `snippets[].snippetDisplayUrl` | string |  |
| `snippets[].snippetTitle` | string |  |
| `snippets[].url` | string |  |
| `trafficSum` | number |  |

## Native endpoint

Through the native SE Ranking Data API, this operation is `GET /domain/ads` (base URL `https://api.seranking.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-paid-ads-by-keyword.md) for the provider-specific parameters and requirements.

