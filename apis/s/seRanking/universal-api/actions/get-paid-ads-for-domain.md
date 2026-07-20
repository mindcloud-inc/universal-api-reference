# SE Ranking Data: Get paid ads for domain

Retrieves paid ads for a domain from SE Ranking Data.

```
GET https://connect.mindcloud.co/v1/universal/seRanking/latest/actions/get-paid-ads-for-domain
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SE Ranking Data `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/seRanking/latest/actions/get-paid-ads-for-domain?connectionId=$CONNECTION_ID&domain=seranking.com&source=us" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "domain": "seranking.com",
  "source": "us"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/seRanking/latest/actions/get-paid-ads-for-domain?${params}`, {
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
      "adsCount": 1,
      "competition": 1,
      "coverage": 1,
      "cpc": 1,
      "keyword": "string",
      "snippets": [
        "string"
      ],
      "traffic": 1,
      "volume": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `adsCount` | number | Number of detected ads. |
| `competition` | number | Competition score. |
| `coverage` | number | Coverage percentage. |
| `cpc` | number | Cost-per-click estimate. |
| `keyword` | string | Keyword associated with detected ad. |
| `snippets` | array<string> | Detected SERP snippets. |
| `traffic` | number | Estimated traffic. |
| `volume` | number | Search volume. |

## Native endpoint

Through the native SE Ranking Data API, this operation is `GET /domain/ads` (base URL `https://api.seranking.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-paid-ads-for-domain.md) for the provider-specific parameters and requirements.

