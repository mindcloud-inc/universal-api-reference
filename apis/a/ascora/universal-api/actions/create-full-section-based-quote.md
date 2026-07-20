# Ascora: Create Full Section-Based Quote

Creates a new section-based quote in Ascora.

```
POST https://connect.mindcloud.co/v1/universal/ascora/latest/actions/create-full-section-based-quote
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Ascora `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/ascora/latest/actions/create-full-section-based-quote" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/ascora/latest/actions/create-full-section-based-quote', {
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
| `siteCustomer` | object | no |  |
| `pricingMethod` | string | no |  |
| `childQuotes` | list<object> | no |  |
| `quoteName` | string | no |  |
| `quoteDescription` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "quotation": {
        "childQuotes[0]": {
          "quoteNumber": "string"
        },
        "childQuotes[1]": {
          "quoteNumber": "string"
        },
        "pricingMethod": "string",
        "quoteId": "string",
        "quoteName": "Ava Chen",
        "quoteNumber": "string",
        "quoteStatusText": "string",
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
| `quotation.childQuotes[0].quoteNumber` | string | First child quote number. |
| `quotation.childQuotes[1].quoteNumber` | string | Second child quote number. |
| `quotation.pricingMethod` | string | Pricing method. |
| `quotation.quoteId` | string | ID of the created parent quote. |
| `quotation.quoteName` | string | Parent quote name. |
| `quotation.quoteNumber` | string | Parent quote number. |
| `quotation.quoteStatusText` | string | Parent quote status text. |
| `quotation.totalIncTax` | number | Parent total including tax. |
| `success` | boolean | Whether Ascora created the section-based quote. |

## Native endpoint

Through the native Ascora API, this operation is `POST /Quotes/Quote` (base URL `https://api.ascora.com.au`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-full-section-based-quote.md) for the provider-specific parameters and requirements.

