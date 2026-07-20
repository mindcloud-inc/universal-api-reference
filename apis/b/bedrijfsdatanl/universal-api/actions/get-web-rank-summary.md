# Bedrijfsdata.nl: Get Web Rank Summary



```
GET https://connect.mindcloud.co/v1/universal/bedrijfsdatanl/latest/actions/get-web-rank-summary
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Bedrijfsdata.nl `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/bedrijfsdatanl/latest/actions/get-web-rank-summary?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/bedrijfsdatanl/latest/actions/get-web-rank-summary?${params}`, {
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
| `domain` | string | no | Domain to evaluate for web rank data. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "creditsUsed": 1,
      "creditsUsedMonth": 1,
      "monthlyCredits": 1,
      "product": "string",
      "status": "string",
      "webrank": {
        "builtwith": 1,
        "cloudflare": 1,
        "commoncrawl": 1,
        "crux": 1,
        "domain": "string",
        "domcop": 1,
        "hostio": 1,
        "majestic": 1,
        "pagerank": 1,
        "tranco": 1,
        "umbrella": 1,
        "webrank": 1
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `creditsUsed` | number |  |
| `creditsUsedMonth` | number |  |
| `monthlyCredits` | number |  |
| `product` | string |  |
| `status` | string |  |
| `webrank.builtwith` | number |  |
| `webrank.cloudflare` | number |  |
| `webrank.commoncrawl` | number |  |
| `webrank.crux` | number |  |
| `webrank.domain` | string |  |
| `webrank.domcop` | number |  |
| `webrank.hostio` | number |  |
| `webrank.majestic` | number |  |
| `webrank.pagerank` | number |  |
| `webrank.tranco` | number |  |
| `webrank.umbrella` | number |  |
| `webrank.webrank` | number |  |

## Native endpoint

Through the native Bedrijfsdata.nl API, this operation is `GET /webrank` (base URL `https://fapi.bedrijfsdata.nl/v1.2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-web-rank-summary.md) for the provider-specific parameters and requirements.

