# EODHD: Get News Word Weights

Retrieves news word weights for a symbol from EODHD API.

```
GET https://connect.mindcloud.co/v1/universal/eODHDAPI/latest/actions/get-news-word-weights
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a EODHD `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/eODHDAPI/latest/actions/get-news-word-weights?connectionId=$CONNECTION_ID&s=AAPL" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "s": "AAPL"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/eODHDAPI/latest/actions/get-news-word-weights?${params}`, {
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
| `s` | string | yes | Ticker symbol, for example AAPL. Example: `AAPL`. |
| `filterDateFrom` | date | no | Start date for the word-weights date filter in YYYY-MM-DD format. Example: `2025-04-08`. |
| `filterTo` | date | no | End date for the word-weights date filter in YYYY-MM-DD format. Example: `2025-04-16`. |
| `pageLimit` | number | no | Maximum number of word-weight rows to return. Example: `10`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "weight": 1,
      "word": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `weight` | number | Word weight. |
| `word` | string | News word. |

## Native endpoint

Through the native EODHD API, this operation is `GET /news-word-weights` (base URL `https://eodhd.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-news-word-weights.md) for the provider-specific parameters and requirements.

