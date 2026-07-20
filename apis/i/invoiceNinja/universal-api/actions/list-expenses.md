# Invoice Ninja: List Expenses



```
GET https://connect.mindcloud.co/v1/universal/invoiceNinja/latest/actions/list-expenses
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Invoice Ninja `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/invoiceNinja/latest/actions/list-expenses?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/invoiceNinja/latest/actions/list-expenses?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "amount": 1,
      "archivedAt": 1,
      "categoryId": "string",
      "clientId": "string",
      "createdAt": 1,
      "currencyId": "string",
      "date": "string",
      "documents": [
        {}
      ],
      "eInvoice": {},
      "entityType": "string",
      "exchangeRate": 1,
      "id": "string",
      "isDeleted": true,
      "number": "string",
      "paymentTypeId": "string",
      "privateNotes": "string",
      "publicNotes": "string",
      "transactionReference": "string",
      "updatedAt": 1,
      "vendorId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `amount` | number |  |
| `archivedAt` | number |  |
| `categoryId` | string |  |
| `clientId` | string |  |
| `createdAt` | number |  |
| `currencyId` | string |  |
| `date` | string |  |
| `documents` | array<object> |  |
| `eInvoice` | object |  |
| `entityType` | string |  |
| `exchangeRate` | number |  |
| `id` | string |  |
| `isDeleted` | boolean |  |
| `number` | string |  |
| `paymentTypeId` | string |  |
| `privateNotes` | string |  |
| `publicNotes` | string |  |
| `transactionReference` | string |  |
| `updatedAt` | number |  |
| `vendorId` | string |  |

## Native endpoint

Through the native Invoice Ninja API, this operation is `GET /expenses` (base URL `https://invoicing.co/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-expenses.md) for the provider-specific parameters and requirements.

