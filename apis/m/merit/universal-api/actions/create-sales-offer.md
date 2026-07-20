# Merit: Create Sales Offer



```
POST https://connect.mindcloud.co/v1/universal/merit/latest/actions/create-sales-offer
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Merit `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/merit/latest/actions/create-sales-offer" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "Customer": {},
  "DocDate": "string",
  "ExpireDate": "string",
  "OfferNo": "string",
  "OfferRow[]": [
    {}
  ],
  "TaxAmount[]": [
    {}
  ],
  "TotalAmount": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/merit/latest/actions/create-sales-offer', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "Customer": {},
    "DocDate": "string",
    "ExpireDate": "string",
    "OfferNo": "string",
    "OfferRow[]": [{}],
    "TaxAmount[]": [{}],
    "TotalAmount": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `Customer` | object | yes | Customer object, for example {"Id":"..."}. |
| `DocDate` | string | yes | Offer date in Merit date string format. |
| `ExpireDate` | string | yes | Offer expiry date in Merit date string format. |
| `OfferNo` | string | yes | Sales offer number. |
| `DocType` | number | no | Sales offer type code. Default: `1`. |
| `OfferRow[]` | array<object> | yes | Array of offer row objects. |
| `TaxAmount[]` | array<object> | yes | Array of tax amount objects. |
| `TotalAmount` | number | yes | Offer total amount. |
| `CurrencyCode` | string | no | Currency code, for example EUR. Default: `EUR`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "CustomerId": "string",
      "InvoiceId": "string",
      "InvoiceNo": "string",
      "NewCustomer": "string",
      "RefNo": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `CustomerId` | string | Customer identifier linked to the created sales offer. |
| `InvoiceId` | string | Created sales offer identifier returned by Merit. |
| `InvoiceNo` | string | Created sales offer number returned by Merit. |
| `NewCustomer` | string | New customer identifier when Merit created a customer inline. |
| `RefNo` | string | Reference number when present. |

## Native endpoint

Through the native Merit API, this operation is `POST v2/sendoffer` (base URL `https://aktiva.merit.ee/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-sales-offer.md) for the provider-specific parameters and requirements.

