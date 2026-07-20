# Finnhub: Get Market Status

Retrieves market status from Finnhub.

```
GET https://connect.mindcloud.co/v1/universal/finnhub/latest/actions/get-market-status
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Finnhub `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/finnhub/latest/actions/get-market-status?connectionId=$CONNECTION_ID&exchange=e.g.%20US" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "exchange": "e.g. US"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/finnhub/latest/actions/get-market-status?${params}`, {
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
| `exchange` | string | yes | Exchange code for current market status, such as US. Example: `e.g. US`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "exchange": "string",
      "holiday": "string",
      "isOpen": true,
      "session": "string",
      "t": 1,
      "timezone": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `exchange` | string |  |
| `holiday` | string |  |
| `isOpen` | boolean |  |
| `session` | string |  |
| `t` | number |  |
| `timezone` | string |  |

## Native endpoint

Through the native Finnhub API, this operation is `GET /stock/market-status` (base URL `https://finnhub.io/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-market-status.md) for the provider-specific parameters and requirements.

