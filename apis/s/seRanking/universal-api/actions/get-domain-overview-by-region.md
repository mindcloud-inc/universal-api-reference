# SE Ranking Data: Get Domain Overview by Region

Retrieves a regional domain overview from SE Ranking Data.

```
GET https://connect.mindcloud.co/v1/universal/seRanking/latest/actions/get-domain-overview-by-region
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SE Ranking Data `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/seRanking/latest/actions/get-domain-overview-by-region?connectionId=$CONNECTION_ID&source=us&domain=seranking.com" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "source": "us",
  "domain": "seranking.com"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/seRanking/latest/actions/get-domain-overview-by-region?${params}`, {
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
| `source` | string | yes | Database region code (for example: us, gb). Example: `us`. |
| `domain` | string | yes | Domain to analyze (for example: seranking.com). Example: `seranking.com`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `withSubdomains` | list<string> | no | Include subdomain data (1/0). One of: `0`, `1`. Example: `1`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "adv": {
        "baseDomain": "string",
        "keywordsCount": 1,
        "keywordsDownCount": 1,
        "keywordsEqualCount": 1,
        "keywordsLostCount": 1,
        "keywordsNewCount": 1,
        "keywordsUpCount": 1,
        "month": 1,
        "priceSum": 1,
        "top12": 1,
        "top35": 1,
        "top68": 1,
        "top911": 1,
        "trafficSum": 1,
        "year": 1
      },
      "organic": {
        "baseDomain": "string",
        "keywordsCount": 1,
        "keywordsDownCount": 1,
        "keywordsEqualCount": 1,
        "keywordsLostCount": 1,
        "keywordsNewCount": 1,
        "keywordsUpCount": 1,
        "month": 1,
        "priceSum": 1,
        "top1120": 1,
        "top15": 1,
        "top2150": 1,
        "top51100": 1,
        "top610": 1,
        "trafficSum": 1,
        "year": 1
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `adv` | object | Paid advertising overview metrics for the requested domain and database. |
| `adv.baseDomain` | string |  |
| `adv.keywordsCount` | number |  |
| `adv.keywordsDownCount` | number |  |
| `adv.keywordsEqualCount` | number |  |
| `adv.keywordsLostCount` | number |  |
| `adv.keywordsNewCount` | number |  |
| `adv.keywordsUpCount` | number |  |
| `adv.month` | number |  |
| `adv.priceSum` | number |  |
| `adv.top12` | number |  |
| `adv.top35` | number |  |
| `adv.top68` | number |  |
| `adv.top911` | number |  |
| `adv.trafficSum` | number |  |
| `adv.year` | number |  |
| `organic` | object | Organic overview metrics for the requested domain and database. |
| `organic.baseDomain` | string |  |
| `organic.keywordsCount` | number |  |
| `organic.keywordsDownCount` | number |  |
| `organic.keywordsEqualCount` | number |  |
| `organic.keywordsLostCount` | number |  |
| `organic.keywordsNewCount` | number |  |
| `organic.keywordsUpCount` | number |  |
| `organic.month` | number |  |
| `organic.priceSum` | number |  |
| `organic.top1120` | number |  |
| `organic.top15` | number |  |
| `organic.top2150` | number |  |
| `organic.top51100` | number |  |
| `organic.top610` | number |  |
| `organic.trafficSum` | number |  |
| `organic.year` | number |  |

## Native endpoint

Through the native SE Ranking Data API, this operation is `GET /domain/overview/db` (base URL `https://api.seranking.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-domain-overview-by-region.md) for the provider-specific parameters and requirements.

