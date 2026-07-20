# Finnhub: List Company Peers

Retrieves company peers from Finnhub.

```
GET https://connect.mindcloud.co/v1/universal/finnhub/latest/actions/list-company-peers
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Finnhub `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/finnhub/latest/actions/list-company-peers?connectionId=$CONNECTION_ID&symbol=e.g.%20AAPL" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "symbol": "e.g. AAPL"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/finnhub/latest/actions/list-company-peers?${params}`, {
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
| `symbol` | string | yes | Company symbol, such as AAPL. Example: `e.g. AAPL`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `grouping` | string | no | Optional peer grouping: sector, industry, or subIndustry. Example: `e.g. subIndustry`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "peers": [
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
| `peers` | array<string> |  |

## Native endpoint

Through the native Finnhub API, this operation is `GET /stock/peers` (base URL `https://finnhub.io/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-company-peers.md) for the provider-specific parameters and requirements.

