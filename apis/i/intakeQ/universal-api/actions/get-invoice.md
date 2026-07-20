# IntakeQ: Get Invoice

Retrieves an invoice from IntakeQ.

```
GET https://connect.mindcloud.co/v1/universal/intakeQ/latest/actions/get-invoice
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a IntakeQ `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/intakeQ/latest/actions/get-invoice?connectionId=$CONNECTION_ID&invoiceId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "invoiceId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/intakeQ/latest/actions/get-invoice?${params}`, {
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
| `invoiceId` | string | yes | The IntakeQ invoice ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "amountDue": 1,
      "amountPaid": 1,
      "clientEmail": "ava@example.com",
      "clientId": "string",
      "clientIdNumber": 1,
      "clientName": "Ava Chen",
      "currencyIso": "string",
      "dateCreated": 1,
      "diagnosisList": [
        "string"
      ],
      "dueDate": 1,
      "id": "string",
      "issuedDate": 1,
      "items": [
        {}
      ],
      "lastModified": 1,
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
| `clientId` | string |  |
| `clientIdNumber` | number |  |
| `clientName` | string |  |
| `currencyIso` | string |  |
| `dateCreated` | number |  |
| `diagnosisList` | array<string> |  |
| `dueDate` | number |  |
| `id` | string |  |
| `issuedDate` | number |  |
| `items` | array<object> |  |
| `lastModified` | number |  |
| `number` | number |  |
| `payments` | array<object> |  |
| `status` | string |  |
| `subTotal` | number |  |
| `totalAmount` | number |  |

## Native endpoint

Through the native IntakeQ API, this operation is `GET /invoices/{invoiceId}` (base URL `https://intakeq.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-invoice.md) for the provider-specific parameters and requirements.

