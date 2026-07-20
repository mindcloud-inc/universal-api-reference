# EODHD: List Historical Splits

Retrieves historical splits for a symbol from EODHD API.

```
GET https://connect.mindcloud.co/v1/universal/eODHDAPI/latest/actions/list-historical-splits
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a EODHD `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/eODHDAPI/latest/actions/list-historical-splits?connectionId=$CONNECTION_ID&symbol=AAPL.US" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "symbol": "AAPL.US"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/eODHDAPI/latest/actions/list-historical-splits?${params}`, {
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
| `from` | date | no | Start date in `YYYY-MM-DD` format. Example: `2000-01-01`. |
| `to` | date | no | End date in `YYYY-MM-DD` format. Example: `2025-12-31`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "date": "2026-05-07T12:00:00.000Z",
      "split": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `date` | date | Split date. |
| `split` | string | Split ratio. |

## Native endpoint

Through the native EODHD API, this operation is `GET /splits/{symbol}` (base URL `https://eodhd.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-historical-splits.md) for the provider-specific parameters and requirements.

