# Finnhub: Get Market News

Retrieves market news from Finnhub.

```
GET https://connect.mindcloud.co/v1/universal/finnhub/latest/actions/get-market-news
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Finnhub `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/finnhub/latest/actions/get-market-news?connectionId=$CONNECTION_ID&category=e.g.%20general" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "category": "e.g. general"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/finnhub/latest/actions/get-market-news?${params}`, {
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
| `category` | string | yes | Market news category: general, forex, crypto, or merger. Example: `e.g. general`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `minId` | number | no | Optional news ID lower bound for fetching newer items. Example: `e.g. 0`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "category": "string",
      "datetime": 1,
      "headline": "string",
      "id": 1,
      "image": "string",
      "related": "string",
      "source": "string",
      "summary": "string",
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `category` | string |  |
| `datetime` | number |  |
| `headline` | string |  |
| `id` | number |  |
| `image` | string |  |
| `related` | string |  |
| `source` | string |  |
| `summary` | string |  |
| `url` | string |  |

## Native endpoint

Through the native Finnhub API, this operation is `GET /news` (base URL `https://finnhub.io/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-market-news.md) for the provider-specific parameters and requirements.

