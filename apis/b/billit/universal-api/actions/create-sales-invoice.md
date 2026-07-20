# Billit: Create Sales Invoice

Creates a sales invoice in Billit.

```
POST https://connect.mindcloud.co/v1/universal/billit/latest/actions/create-sales-invoice
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Billit `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/billit/latest/actions/create-sales-invoice" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "OrderNumber": "string",
  "OrderDate": "2026-05-07T12:00:00.000Z",
  "ExpiryDate": "2026-05-07T12:00:00.000Z",
  "Customer": {},
  "OrderLines[]": [
    {}
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/billit/latest/actions/create-sales-invoice', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "OrderNumber": "string",
    "OrderDate": "2026-05-07T12:00:00.000Z",
    "ExpiryDate": "2026-05-07T12:00:00.000Z",
    "Customer": {},
    "OrderLines[]": [{}]
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `OrderNumber` | string | yes | Unique invoice number from your source system. |
| `OrderDate` | date | yes | Invoice issue date in YYYY-MM-DD format. |
| `DeliveryDate` | date | no | Delivery date in YYYY-MM-DD format. |
| `ExpiryDate` | date | yes | Invoice due date in YYYY-MM-DD format. |
| `Customer` | object | yes | Billit customer object; include Name, PartyType, VATNumber or address details as needed. |
| `OrderLines[]` | array<object> | yes | Array of Billit order line objects. |
| `Reference` | string | no | Optional buyer purchase-order reference. |
| `Currency` | string | no | Optional ISO currency code; Billit defaults to EUR when omitted. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | number | New Billit OrderID returned after invoice creation. |

## Native endpoint

Through the native Billit API, this operation is `POST /v1/orders` (base URL `https://api.sandbox.billit.be`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-sales-invoice.md) for the provider-specific parameters and requirements.

