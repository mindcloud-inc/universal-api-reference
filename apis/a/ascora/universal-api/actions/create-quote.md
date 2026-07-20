# Ascora: Create Quote

Creates a new quote in Ascora.

```
POST https://connect.mindcloud.co/v1/universal/ascora/latest/actions/create-quote
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Ascora `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/ascora/latest/actions/create-quote" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/ascora/latest/actions/create-quote', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `siteCustomer.id` | string | no |  |
| `billingCustomer.id` | string | no |  |
| `quoteName` | string | no |  |
| `quoteDescription` | string | no |  |
| `quotationDate` | string | no |  |
| `pricingMethod` | string | no |  |
| `purchaseOrderNumber` | string | no |  |
| `clientOrderNumber` | string | no |  |
| `addressLine1` | string | no |  |
| `addressLine2` | string | no |  |
| `suburb` | string | no |  |
| `postcode` | string | no |  |
| `country` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "quotation": {
        "billingCustomer": {
          "name": "Ava Chen"
        },
        "pricingMethod": "string",
        "quoteDescription": "string",
        "quoteId": "string",
        "quoteName": "Ava Chen",
        "quoteNumber": "string",
        "quoteStatusText": "string",
        "siteCustomer": {
          "name": "Ava Chen"
        },
        "totalIncTax": 1
      },
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `quotation.billingCustomer.name` | string | Billing customer name. |
| `quotation.pricingMethod` | string | Pricing method. |
| `quotation.quoteDescription` | string | Quote description. |
| `quotation.quoteId` | string | ID of the created quote. |
| `quotation.quoteName` | string | Quote name. |
| `quotation.quoteNumber` | string | Quote number. |
| `quotation.quoteStatusText` | string | Quote status text. |
| `quotation.siteCustomer.name` | string | Site customer name. |
| `quotation.totalIncTax` | number | Total including tax. |
| `success` | boolean | Whether Ascora created the quote. |

## Native endpoint

Through the native Ascora API, this operation is `POST /Quotes/Quote` (base URL `https://api.ascora.com.au`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-quote.md) for the provider-specific parameters and requirements.

