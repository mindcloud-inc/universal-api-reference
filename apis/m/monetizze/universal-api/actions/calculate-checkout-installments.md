# Monetizze: Calculate Checkout Installments

Retrieves transparent checkout installment options from Monetizze.

```
GET https://connect.mindcloud.co/v1/universal/monetizze/latest/actions/calculate-checkout-installments
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Monetizze `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/monetizze/latest/actions/calculate-checkout-installments?connectionId=$CONNECTION_ID&ctk=string&reference=string&value=1&maxInstallments=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "ctk": "string",
  "reference": "string",
  "value": "1",
  "maxInstallments": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/monetizze/latest/actions/calculate-checkout-installments?${params}`, {
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
| `ctk` | string | yes | Checkout transparent CTK environment key. |
| `reference` | string | yes | Product checkout reference used by Monetizze. |
| `value` | number | yes | Order value used to calculate installments. |
| `maxInstallments` | number | yes | Maximum number of installments to calculate. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "msg": "string",
      "status": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `msg` | string | Installment calculation message returned by Monetizze. |
| `status` | number | Installment calculation status returned by Monetizze. |

## Native endpoint

Through the native Monetizze API, this operation is `POST https://app.monetizze.com.br/checkout/transparente/parcelamento` (base URL `https://api.monetizze.com.br/2.1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/calculate-checkout-installments.md) for the provider-specific parameters and requirements.

