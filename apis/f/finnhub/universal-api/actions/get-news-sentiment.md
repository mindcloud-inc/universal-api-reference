# Finnhub: Get News Sentiment

Retrieves news sentiment from Finnhub.

```
GET https://connect.mindcloud.co/v1/universal/finnhub/latest/actions/get-news-sentiment
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Finnhub `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/finnhub/latest/actions/get-news-sentiment?connectionId=$CONNECTION_ID&symbol=e.g.%20AAPL" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "symbol": "e.g. AAPL"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/finnhub/latest/actions/get-news-sentiment?${params}`, {
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
| `symbol` | string | yes | US company symbol for news sentiment, such as AAPL. Example: `e.g. AAPL`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "buzz": {
        "articlesInLastWeek": 1,
        "buzz": 1,
        "weeklyAverage": 1
      },
      "companyNewsScore": 1,
      "sectorAverageBullishPercent": 1,
      "sectorAverageNewsScore": 1,
      "sentiment": {
        "bearishPercent": 1,
        "bullishPercent": 1
      },
      "symbol": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `buzz.articlesInLastWeek` | number |  |
| `buzz.buzz` | number |  |
| `buzz.weeklyAverage` | number |  |
| `companyNewsScore` | number |  |
| `sectorAverageBullishPercent` | number |  |
| `sectorAverageNewsScore` | number |  |
| `sentiment.bearishPercent` | number |  |
| `sentiment.bullishPercent` | number |  |
| `symbol` | string |  |

## Native endpoint

Through the native Finnhub API, this operation is `GET /news-sentiment` (base URL `https://finnhub.io/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-news-sentiment.md) for the provider-specific parameters and requirements.

