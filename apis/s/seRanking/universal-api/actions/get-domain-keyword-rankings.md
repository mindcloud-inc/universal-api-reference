# SE Ranking Data: Get Domain Keyword Rankings

Retrieves domain keyword rankings from SE Ranking Data.

```
GET https://connect.mindcloud.co/v1/universal/seRanking/latest/actions/get-domain-keyword-rankings
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SE Ranking Data `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/seRanking/latest/actions/get-domain-keyword-rankings?connectionId=$CONNECTION_ID&limit=25&offset=0&source=us&domain=seranking.com" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "source": "us",
  "domain": "seranking.com"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/seRanking/latest/actions/get-domain-keyword-rankings?${params}`, {
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
| `source` | string | yes | Database region code (for example: us). Example: `us`. |
| `domain` | string | yes | Domain to retrieve ranking keywords for (for example: seranking.com). Example: `seranking.com`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "cpc": 1,
      "difficulty": 1,
      "intents": [
        "string"
      ],
      "keyword": "string",
      "position": 1,
      "prevPos": 1,
      "price": 1,
      "serpFeatures": [
        "string"
      ],
      "traffic": 1,
      "url": "https://example.com",
      "volume": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `cpc` | number | Cost-per-click estimate. |
| `difficulty` | number | Keyword difficulty score. |
| `intents` | array<string> | Search intent codes. |
| `keyword` | string | Keyword phrase. |
| `position` | number | Current ranking position. |
| `prevPos` | number | Previous ranking position. |
| `price` | number | Estimated traffic value. |
| `serpFeatures` | array<string> | SERP feature flags. |
| `traffic` | number | Estimated traffic. |
| `url` | string | Ranking URL. |
| `volume` | number | Search volume. |

## Native endpoint

Through the native SE Ranking Data API, this operation is `GET /domain/keywords` (base URL `https://api.seranking.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/get-domain-keyword-rankings.md) for the provider-specific parameters and requirements.

