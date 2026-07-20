# IntakeQ: Query Invoices

Retrieves invoices from IntakeQ.

```
GET https://connect.mindcloud.co/v1/universal/intakeQ/latest/actions/query-invoices
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a IntakeQ `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/intakeQ/latest/actions/query-invoices?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/intakeQ/latest/actions/query-invoices?${params}`, {
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
      "amountDue": 1,
      "amountPaid": 1,
      "clientEmail": "ava@example.com",
      "clientIdNumber": 1,
      "clientName": "Ava Chen",
      "currencyIso": "string",
      "dateCreated": 1,
      "dueDate": 1,
      "id": "string",
      "issuedDate": 1,
      "items": [
        {}
      ],
      "number": 1,
      "payments": [
        {}
      ],
      "status": "string",
      "subTotal": 1,
      "totalAmount": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `amountDue` | number |  |
| `amountPaid` | number |  |
| `clientEmail` | string |  |
| `clientIdNumber` | number |  |
| `clientName` | string |  |
| `currencyIso` | string |  |
| `dateCreated` | number |  |
| `dueDate` | number |  |
| `id` | string |  |
| `issuedDate` | number |  |
| `items` | array<object> |  |
| `number` | number |  |
| `payments` | array<object> |  |
| `status` | string |  |
| `subTotal` | number |  |
| `totalAmount` | number |  |

## Native endpoint

Through the native IntakeQ API, this operation is `GET /invoices` (base URL `https://intakeq.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/query-invoices.md) for the provider-specific parameters and requirements.

