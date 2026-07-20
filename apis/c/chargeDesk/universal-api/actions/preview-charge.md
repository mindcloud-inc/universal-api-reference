# ChargeDesk: Preview Charge

Retrieves a charge preview from ChargeDesk.

```
GET https://connect.mindcloud.co/v1/universal/chargeDesk/latest/actions/preview-charge
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ChargeDesk `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/chargeDesk/latest/actions/preview-charge?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/chargeDesk/latest/actions/preview-charge?${params}`, {
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
| `chargeId` | string | no | Charge to preview. |
| `productId` | string | no | Product to preview. Ignored if Charge ID is also provided. |
| `amount` | string | no | Amount to preview. Required if no charge or product is provided; otherwise overrides the charge or product amount. |
| `currency` | string | no | Currency to preview. Required if no charge or product is provided; otherwise overrides the charge or product currency. |
| `country` | string | no | Two-letter ISO country code for the customer location. |
| `taxNumber` | string | no | Customer tax identification number used to determine whether 0% tax should apply. |
| `addTax` | boolean | no | Override the company setting for whether tax is added to or included in the final amount. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "subtotalAmount": 1,
      "subtotalAmountFormatted": "string",
      "taxRates": [
        {}
      ],
      "totalAmount": 1,
      "totalAmountFormatted": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `subtotalAmount` | number |  |
| `subtotalAmountFormatted` | string |  |
| `taxRates` | array<object> |  |
| `totalAmount` | number |  |
| `totalAmountFormatted` | string |  |

## Native endpoint

Through the native ChargeDesk API, this operation is `GET /charges/preview` (base URL `https://api.chargedesk.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/preview-charge.md) for the provider-specific parameters and requirements.

