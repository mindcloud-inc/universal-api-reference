# EODHD: Get Share Statistics

Retrieves share statistics for a symbol from EODHD API.

```
GET https://connect.mindcloud.co/v1/universal/eODHDAPI/latest/actions/get-share-statistics
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a EODHD `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/eODHDAPI/latest/actions/get-share-statistics?connectionId=$CONNECTION_ID&symbol=AAPL.US" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "symbol": "AAPL.US"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/eODHDAPI/latest/actions/get-share-statistics?${params}`, {
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
| `symbol` | string | yes | EODHD ticker in `{symbol}.{exchange}` format, such as `AAPL.US`. Example: `AAPL.US`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "PercentInsiders": 1,
      "PercentInstitutions": 1,
      "SharesFloat": 1,
      "SharesOutstanding": 1,
      "SharesShort": 1,
      "SharesShortPriorMonth": 1,
      "ShortPercentFloat": 1,
      "ShortPercentOutstanding": 1,
      "ShortRatio": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `PercentInsiders` | number | Insider ownership percentage. |
| `PercentInstitutions` | number | Institutional ownership percentage. |
| `SharesFloat` | number | Shares float. |
| `SharesOutstanding` | number | Shares outstanding. |
| `SharesShort` | number | Shares short. |
| `SharesShortPriorMonth` | number | Prior-month shares short. |
| `ShortPercentFloat` | number | Short percentage of float. |
| `ShortPercentOutstanding` | number | Short percentage of outstanding shares. |
| `ShortRatio` | number | Short ratio. |

## Native endpoint

Through the native EODHD API, this operation is `GET /fundamentals/{symbol}` (base URL `https://eodhd.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-share-statistics.md) for the provider-specific parameters and requirements.

