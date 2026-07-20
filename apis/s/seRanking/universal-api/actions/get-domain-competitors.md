# SE Ranking Data: Get domain competitors

Retrieves domain competitors from SE Ranking Data.

```
GET https://connect.mindcloud.co/v1/universal/seRanking/latest/actions/get-domain-competitors
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SE Ranking Data `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/seRanking/latest/actions/get-domain-competitors?connectionId=$CONNECTION_ID&domain=seranking.com&source=us" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "domain": "seranking.com",
  "source": "us"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/seRanking/latest/actions/get-domain-competitors?${params}`, {
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
| `domain` | string | yes | Domain to analyze (for example: seranking.com). Example: `seranking.com`. |
| `source` | string | yes | Regional database code (for example: us). Example: `us`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "commonKeywords": 1,
      "domain": "string",
      "domainRelevance": 1,
      "missingKeywords": 1,
      "priceSum": 1,
      "totalKeywords": 1,
      "trafficSum": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `commonKeywords` | number |  |
| `domain` | string |  |
| `domainRelevance` | number |  |
| `missingKeywords` | number |  |
| `priceSum` | number |  |
| `totalKeywords` | number |  |
| `trafficSum` | number |  |

## Native endpoint

Through the native SE Ranking Data API, this operation is `GET /domain/competitors` (base URL `https://api.seranking.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-domain-competitors.md) for the provider-specific parameters and requirements.

