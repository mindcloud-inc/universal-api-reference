# Becon: Get Current Address

Retrieves the latest payment address from Becon.

```
GET https://connect.mindcloud.co/v1/universal/becon/latest/actions/get-current-address
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Becon `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/becon/latest/actions/get-current-address?connectionId=$CONNECTION_ID&external_id=string&origin_amount=string&origin_currency=string&payment_currency=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "external_id": "string",
  "origin_amount": "string",
  "origin_currency": "string",
  "payment_currency": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/becon/latest/actions/get-current-address?${params}`, {
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
| `chain` | string | no | Target network: bitcoin, binance, ethereum, or tron. |
| `external_id` | string | yes | Unique tracking value returned in callbacks. |
| `origin_amount` | string | yes | Amount in the origin currency for automatic conversion. |
| `origin_currency` | string | yes | Origin fiat currency, for example USD or EUR. |
| `payment_amount` | string | no | Optional fixed payment amount to override automatic conversion. |
| `payment_currency` | string | yes | Token ticker to accept, for example USDC or BTC. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "address": "string",
      "message": "string",
      "payment_amount": "string",
      "payment_currency": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `address` | string | Current payment address. |
| `message` | string | Provider message. |
| `payment_amount` | string | Amount that must be paid. |
| `payment_currency` | string | Token ticker to pay. |

## Native endpoint

Through the native Becon API, this operation is `POST /v2/address?reset=1` (base URL `https://external-api.bcon.global/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-current-address.md) for the provider-specific parameters and requirements.

