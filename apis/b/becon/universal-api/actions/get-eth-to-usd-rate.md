# Becon: Get ETH to USD Rate

Retrieves the ETH-to-USD rate from Becon.

```
GET https://connect.mindcloud.co/v1/universal/becon/latest/actions/get-eth-to-usd-rate
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Becon `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/becon/latest/actions/get-eth-to-usd-rate?connectionId=$CONNECTION_ID&cryptoCurrencyName=eth&currency=usd" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "cryptoCurrencyName": "eth",
  "currency": "usd"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/becon/latest/actions/get-eth-to-usd-rate?${params}`, {
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
| `cryptoCurrencyName` | string | yes | The cryptocurrency code in the path, such as eth. Default: `eth`. |
| `currency` | string | yes | The fiat or quote currency code for the requested rate. Default: `usd`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "price": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `price` | string | Quoted conversion rate. |

## Native endpoint

Through the native Becon API, this operation is `GET /v1/currencies/:cryptoCurrencyName` (base URL `https://external-api.bcon.global/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-eth-to-usd-rate.md) for the provider-specific parameters and requirements.

