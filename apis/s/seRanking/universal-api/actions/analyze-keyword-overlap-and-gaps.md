# SE Ranking Data: Analyze keyword overlap and gaps

Analyzes keyword overlap and gaps in SE Ranking Data.

```
GET https://connect.mindcloud.co/v1/universal/seRanking/latest/actions/analyze-keyword-overlap-and-gaps
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SE Ranking Data `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/seRanking/latest/actions/analyze-keyword-overlap-and-gaps?connectionId=$CONNECTION_ID&compare=example.com&domain=seranking.com&source=us" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "compare": "example.com",
  "domain": "seranking.com",
  "source": "us"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/seRanking/latest/actions/analyze-keyword-overlap-and-gaps?${params}`, {
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
| `compare` | string | yes | Competitor domain or URL for comparison (for example: example.com). Example: `example.com`. |
| `domain` | string | yes | Primary domain for comparison (for example: seranking.com). Example: `seranking.com`. |
| `source` | string | yes | Regional database code (for example: us). Example: `us`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "comparePosition": 1,
      "comparePrice": 1,
      "compareTraffic": 1,
      "compareUrl": "https://example.com",
      "competition": 1,
      "cpc": 1,
      "difficulty": 1,
      "keyword": "string",
      "position": 1,
      "price": 1,
      "totalSites": 1,
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
| `comparePosition` | number |  |
| `comparePrice` | number |  |
| `compareTraffic` | number |  |
| `compareUrl` | string |  |
| `competition` | number |  |
| `cpc` | number |  |
| `difficulty` | number |  |
| `keyword` | string |  |
| `position` | number |  |
| `price` | number |  |
| `totalSites` | number |  |
| `traffic` | number |  |
| `url` | string |  |
| `volume` | number |  |

## Native endpoint

Through the native SE Ranking Data API, this operation is `GET /domain/keywords/comparison` (base URL `https://api.seranking.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/analyze-keyword-overlap-and-gaps.md) for the provider-specific parameters and requirements.

