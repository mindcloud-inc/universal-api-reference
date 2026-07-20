# CoinGate: List Supported Payment Currencies

Retrieves supported payment currencies from CoinGate.

```
GET https://connect.mindcloud.co/v1/universal/coinGate/latest/actions/list-supported-payment-currencies
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a CoinGate `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/coinGate/latest/actions/list-supported-payment-currencies?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/coinGate/latest/actions/list-supported-payment-currencies?${params}`, {
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
      "currencies": [
        {
          "id": 1,
          "kind": "string",
          "native": true,
          "symbol": "string",
          "title": "string"
        }
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `currencies[].id` | number |  |
| `currencies[].kind` | string |  |
| `currencies[].native` | boolean |  |
| `currencies[].symbol` | string |  |
| `currencies[].title` | string |  |

## Native endpoint

Through the native CoinGate API, this operation is `GET /currencies` (base URL `https://api.coingate.com/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-supported-payment-currencies.md) for the provider-specific parameters and requirements.

