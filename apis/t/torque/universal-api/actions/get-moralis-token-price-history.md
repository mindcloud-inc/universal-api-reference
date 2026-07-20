# Torque: Get Moralis Token Price History



```
GET https://connect.mindcloud.co/v1/universal/torque/latest/actions/get-moralis-token-price-history
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Torque `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/torque/latest/actions/get-moralis-token-price-history?connectionId=$CONNECTION_ID&symbol=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "symbol": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/torque/latest/actions/get-moralis-token-price-history?${params}`, {
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
| `symbol` | string | yes | Token symbol. Torque's live endpoint currently requires symbol for this route. |
| `chain` | string | no |  |
| `timeframe` | list | no | One of: `0`, `1`, `2`, `3`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "price": 1,
      "timestamp": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `price` | number |  |
| `timestamp` | number |  |

## Native endpoint

Through the native Torque API, this operation is `GET /moralis/token-price-history` (base URL `https://app.torque.fi/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-moralis-token-price-history.md) for the provider-specific parameters and requirements.

