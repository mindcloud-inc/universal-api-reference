# Ascora: Get Quote

Retrieves a quote from Ascora.

```
GET https://connect.mindcloud.co/v1/universal/ascora/latest/actions/get-quote
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Ascora `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/ascora/latest/actions/get-quote?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/ascora/latest/actions/get-quote?${params}`, {
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
| `quoteNumber` | string | no | Ascora quote number. For sections, use dashes instead of dots, for example Q1234-01. |

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
        "childQuotes": [
          {}
        ],
        "pricingMethod": "string",
        "quoteDescription": "string",
        "quoteId": "string",
        "quoteName": "Ava Chen",
        "quoteNumber": "string",
        "quoteStatusText": "string",
        "siteCustomer": {
          "name": "Ava Chen"
        },
        "totalExTax": 1,
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
| `quotation.childQuotes` | array<object> | Child quote sections when the quote uses SECTIONS pricing. |
| `quotation.pricingMethod` | string | Quote pricing method. |
| `quotation.quoteDescription` | string | Quote description. |
| `quotation.quoteId` | string | Ascora quote ID. |
| `quotation.quoteName` | string | Quote name. |
| `quotation.quoteNumber` | string | Ascora quote number. |
| `quotation.quoteStatusText` | string | Human-readable quote status. |
| `quotation.siteCustomer.name` | string | Site customer name. |
| `quotation.totalExTax` | number | Total quote value excluding tax. |
| `quotation.totalIncTax` | number | Total quote value including tax. |
| `success` | boolean | Whether Ascora returned the quote. |

## Native endpoint

Through the native Ascora API, this operation is `GET /Quotes/Quote/{{quoteNumber}}` (base URL `https://api.ascora.com.au`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-quote.md) for the provider-specific parameters and requirements.

