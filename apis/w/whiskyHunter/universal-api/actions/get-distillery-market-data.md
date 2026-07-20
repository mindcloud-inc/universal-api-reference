# Whisky Hunter: Get Distillery Market Data

Retrieves market data for one Whisky Hunter distillery.

```
GET https://connect.mindcloud.co/v1/universal/whiskyHunter/latest/actions/get-distillery-market-data
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Whisky Hunter `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/whiskyHunter/latest/actions/get-distillery-market-data?connectionId=$CONNECTION_ID&slug=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "slug": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/whiskyHunter/latest/actions/get-distillery-market-data?${params}`, {
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
| `slug` | string | yes | Distillery slug from the Whisky Hunter distilleries list, for example ardbeg. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "dt": "2026-05-07T12:00:00.000Z",
      "lots_count": 1,
      "name": "Ava Chen",
      "slug": "string",
      "trading_volume": 1,
      "winning_bid_max": 1,
      "winning_bid_mean": 1,
      "winning_bid_min": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `dt` | date | Distillery data month. |
| `lots_count` | number | Lots counted for this distillery and month. |
| `name` | string | Distillery name. |
| `slug` | string | Distillery slug used by Whisky Hunter. |
| `trading_volume` | number | Total trading volume for this distillery and month. |
| `winning_bid_max` | number | Highest winning bid for this distillery and month. |
| `winning_bid_mean` | number | Average winning bid for this distillery and month. |
| `winning_bid_min` | number | Lowest winning bid for this distillery and month. |

## Native endpoint

Through the native Whisky Hunter API, this operation is `GET /distillery_data/[:slug]/` (base URL `https://whiskyhunter.net/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-distillery-market-data.md) for the provider-specific parameters and requirements.

