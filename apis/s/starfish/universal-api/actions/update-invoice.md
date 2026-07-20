# Starfish: Update Invoice

Updates an existing invoice in Starfish.

```
PUT https://connect.mindcloud.co/v1/universal/starfish/latest/actions/update-invoice
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Starfish `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/starfish/latest/actions/update-invoice" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "invoiceId": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/starfish/latest/actions/update-invoice', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "invoiceId": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `invoiceId` | number | yes | Invoice ID. |
| `meta0` | string | no | Invoice meta update payload. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "adminId": 1,
      "contact": {},
      "contactId": 1,
      "contactName": "Ava Chen",
      "createDate": "2026-05-07T12:00:00.000Z",
      "currency": "string",
      "id": 1,
      "invoiceId": 1,
      "invoiceUid": "string",
      "lastModified": "2026-05-07T12:00:00.000Z",
      "meta": [
        {}
      ],
      "payments": [
        {}
      ],
      "paymentTerms": [
        {}
      ],
      "reservation": {},
      "reservationId": 1,
      "rows": [
        {}
      ],
      "status": "string",
      "subtotal": 1,
      "total": 1,
      "type": "string",
      "vat": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `adminId` | number |  |
| `contact` | object |  |
| `contactId` | number |  |
| `contactName` | string |  |
| `createDate` | date |  |
| `currency` | string |  |
| `id` | number |  |
| `invoiceId` | number |  |
| `invoiceUid` | string |  |
| `lastModified` | date |  |
| `meta` | array<object> |  |
| `payments` | array<object> |  |
| `paymentTerms` | array<object> |  |
| `reservation` | object |  |
| `reservationId` | number |  |
| `rows` | array<object> |  |
| `status` | string |  |
| `subtotal` | number |  |
| `total` | number |  |
| `type` | string |  |
| `vat` | number |  |

## Native endpoint

Through the native Starfish API, this operation is `PUT /invoices/:invoice_id` (base URL `https://api.camping.care/v21`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-invoice.md) for the provider-specific parameters and requirements.

