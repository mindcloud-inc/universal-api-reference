# Whisky Hunter: List Auction Market Data

Retrieves aggregated online auction market data from Whisky Hunter.

```
GET https://connect.mindcloud.co/v1/universal/whiskyHunter/latest/actions/list-auction-market-data
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Whisky Hunter `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/whiskyHunter/latest/actions/list-auction-market-data?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/whiskyHunter/latest/actions/list-auction-market-data?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "all_auctions_lots_count": 1,
      "auction_lots_count": 1,
      "auction_name": "Ava Chen",
      "auction_slug": "string",
      "auction_trading_volume": 1,
      "dt": "2026-05-07T12:00:00.000Z",
      "winning_bid_mean": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `all_auctions_lots_count` | number | Lots counted across all auctions for this month. |
| `auction_lots_count` | number | Lots counted for this auction and month. |
| `auction_name` | string | Auction house name. |
| `auction_slug` | string | Auction slug used by Whisky Hunter. |
| `auction_trading_volume` | number | Total trading volume for this auction and month. |
| `dt` | date | Auction data month. |
| `winning_bid_mean` | number | Average winning bid for this auction and month. |

## Native endpoint

Through the native Whisky Hunter API, this operation is `GET /auctions_data/` (base URL `https://whiskyhunter.net/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-auction-market-data.md) for the provider-specific parameters and requirements.

