# SE Ranking Data: Get Worldwide Domain Overview

Retrieves a worldwide domain overview from SE Ranking Data.

```
GET https://connect.mindcloud.co/v1/universal/seRanking/latest/actions/get-worldwide-domain-overview
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SE Ranking Data `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/seRanking/latest/actions/get-worldwide-domain-overview?connectionId=$CONNECTION_ID&domain=seranking.com" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "domain": "seranking.com"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/seRanking/latest/actions/get-worldwide-domain-overview?${params}`, {
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
| `domain` | string | yes | Domain to analyze worldwide (for example: seranking.com). Example: `seranking.com`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "adv": [
        {
          "keywordsCount": 1,
          "priceSum": 1,
          "source": "string",
          "trafficSum": 1
        }
      ],
      "organic": [
        {
          "keywordsCount": 1,
          "priceSum": 1,
          "source": "string",
          "trafficSum": 1
        }
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `adv` | array<object> | Worldwide paid summary grouped by source. |
| `adv[].keywordsCount` | number |  |
| `adv[].priceSum` | number |  |
| `adv[].source` | string |  |
| `adv[].trafficSum` | number |  |
| `organic` | array<object> | Worldwide organic summary grouped by source. |
| `organic[].keywordsCount` | number |  |
| `organic[].priceSum` | number |  |
| `organic[].source` | string |  |
| `organic[].trafficSum` | number |  |

## Native endpoint

Through the native SE Ranking Data API, this operation is `GET /domain/overview/worldwide` (base URL `https://api.seranking.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-worldwide-domain-overview.md) for the provider-specific parameters and requirements.

