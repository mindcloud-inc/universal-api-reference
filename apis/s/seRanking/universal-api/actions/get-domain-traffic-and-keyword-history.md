# SE Ranking Data: Get domain traffic and keyword history

Retrieves domain traffic and keyword history from SE Ranking Data.

```
GET https://connect.mindcloud.co/v1/universal/seRanking/latest/actions/get-domain-traffic-and-keyword-history
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SE Ranking Data `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/seRanking/latest/actions/get-domain-traffic-and-keyword-history?connectionId=$CONNECTION_ID&domain=seranking.com&source=us&year=2025" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "domain": "seranking.com",
  "source": "us",
  "year": "2025"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/seRanking/latest/actions/get-domain-traffic-and-keyword-history?${params}`, {
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
| `month` | list<string> | no | Optional month number (1-12). One of: `1`, `10`, `11`, `12`, `2`, `3`, `4`, `5`, `6`, `7`, `8`, `9`. Example: `1`. |
| `source` | string | yes | Regional database code (for example: us). Example: `us`. |
| `year` | string | yes | Year in YYYY format. Example: `2025`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "keywordsCount": 1,
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
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `keywordsCount` | number | Tracked keyword count for the period. |
| `month` | number | Month of the snapshot row. |
| `priceSum` | number | Estimated traffic value for the period. |
| `top1120` | number | Keywords ranked in positions 11-20. |
| `top15` | number | Keywords ranked in positions 1-5. |
| `top2150` | number | Keywords ranked in positions 21-50. |
| `top51100` | number | Keywords ranked in positions 51-100. |
| `top610` | number | Keywords ranked in positions 6-10. |
| `trafficSum` | number | Estimated traffic for the period. |
| `year` | number | Year of the snapshot row. |

## Native endpoint

Through the native SE Ranking Data API, this operation is `GET /domain/overview/history` (base URL `https://api.seranking.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-domain-traffic-and-keyword-history.md) for the provider-specific parameters and requirements.

