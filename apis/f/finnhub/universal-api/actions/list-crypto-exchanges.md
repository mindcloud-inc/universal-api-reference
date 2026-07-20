# Finnhub: List Crypto Exchanges

Retrieves crypto exchanges from Finnhub.

```
GET https://connect.mindcloud.co/v1/universal/finnhub/latest/actions/list-crypto-exchanges
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Finnhub `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/finnhub/latest/actions/list-crypto-exchanges?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/finnhub/latest/actions/list-crypto-exchanges?${params}`, {
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
      "exchanges": [
        "string"
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `exchanges` | array<string> | Crypto exchange codes. |

## Native endpoint

Through the native Finnhub API, this operation is `GET /crypto/exchange` (base URL `https://finnhub.io/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-crypto-exchanges.md) for the provider-specific parameters and requirements.

