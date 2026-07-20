# Invoice Ninja: List Payments



```
GET https://connect.mindcloud.co/v1/universal/invoiceNinja/latest/actions/list-payments
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Invoice Ninja `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/invoiceNinja/latest/actions/list-payments?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/invoiceNinja/latest/actions/list-payments?${params}`, {
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
| `clientId` | string | no | Filter by client. |
| `status` | string | no | Filter by payment status. |
| `filter` | string | no | Free-text filter value. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "amount": 1,
      "applied": 1,
      "archivedAt": 1,
      "clientId": "string",
      "createdAt": 1,
      "currencyId": "string",
      "date": "string",
      "documents": [
        {}
      ],
      "exchangeRate": 1,
      "id": "string",
      "isDeleted": true,
      "isManual": true,
      "number": "string",
      "paymentables": [
        {}
      ],
      "privateNotes": "string",
      "refunded": 1,
      "statusId": "string",
      "transactionReference": "string",
      "typeId": "string",
      "updatedAt": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `amount` | number |  |
| `applied` | number |  |
| `archivedAt` | number |  |
| `clientId` | string |  |
| `createdAt` | number |  |
| `currencyId` | string |  |
| `date` | string |  |
| `documents` | array<object> |  |
| `exchangeRate` | number |  |
| `id` | string |  |
| `isDeleted` | boolean |  |
| `isManual` | boolean |  |
| `number` | string |  |
| `paymentables` | array<object> |  |
| `privateNotes` | string |  |
| `refunded` | number |  |
| `statusId` | string |  |
| `transactionReference` | string |  |
| `typeId` | string |  |
| `updatedAt` | number |  |

## Native endpoint

Through the native Invoice Ninja API, this operation is `GET /payments` (base URL `https://invoicing.co/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-payments.md) for the provider-specific parameters and requirements.

