# Becon: Get Current Ethereum Address

Retrieves the latest Ethereum payment address from Becon.

```
GET https://connect.mindcloud.co/v1/universal/becon/latest/actions/get-current-ethereum-address
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Becon `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/becon/latest/actions/get-current-ethereum-address?connectionId=$CONNECTION_ID&chain=ethereum&external_id=string&origin_amount=string&origin_currency=string&payment_currency=ETH" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "chain": "ethereum",
  "external_id": "string",
  "origin_amount": "string",
  "origin_currency": "string",
  "payment_currency": "ETH"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/becon/latest/actions/get-current-ethereum-address?${params}`, {
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
| `chain` | string | yes | The target blockchain for the payment address. Default: `ethereum`. |
| `external_id` | string | yes | The external reference ID for the address request. |
| `origin_amount` | string | yes | The fiat amount to convert into the destination address request. |
| `origin_currency` | string | yes | The fiat currency code for the requested payment amount. |
| `payment_currency` | string | yes | The cryptocurrency or token code to receive. Default: `ETH`. |

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

Through the native Becon API, this operation is `POST /v2/address?reset=1` (base URL `https://external-api.bcon.global/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-current-ethereum-address.md) for the provider-specific parameters and requirements.

