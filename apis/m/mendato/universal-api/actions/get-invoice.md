# Mendato: Get Invoice



```
GET https://connect.mindcloud.co/v1/universal/mendato/latest/actions/get-invoice
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Mendato `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/mendato/latest/actions/get-invoice?connectionId=$CONNECTION_ID&variables=%5Bobject%20Object%5D" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "variables": "[object Object]"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/mendato/latest/actions/get-invoice?${params}`, {
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
| `variables` | object | yes | GraphQL variables object for the Mendato invoice query. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "invoice": {
        "cancelledAt": "2026-05-07T12:00:00.000Z",
        "completedAt": "2026-05-07T12:00:00.000Z",
        "createdAt": "2026-05-07T12:00:00.000Z",
        "dueDate": "2026-05-07T12:00:00.000Z",
        "id": "string",
        "invoiceDate": "2026-05-07T12:00:00.000Z",
        "isNegative": true,
        "number": 1,
        "numberPrefix": "string",
        "numberSuffix": "string",
        "paidAt": "2026-05-07T12:00:00.000Z",
        "sentAt": "2026-05-07T12:00:00.000Z",
        "sentManually": true,
        "skontoApplied": true,
        "skontoEnabled": true,
        "status": "string",
        "totalAmount": 1,
        "totalNetAmount": 1,
        "type": "string"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `invoice.cancelledAt` | date |  |
| `invoice.completedAt` | date |  |
| `invoice.createdAt` | date |  |
| `invoice.dueDate` | date |  |
| `invoice.id` | string |  |
| `invoice.invoiceDate` | date |  |
| `invoice.isNegative` | boolean |  |
| `invoice.number` | number |  |
| `invoice.numberPrefix` | string |  |
| `invoice.numberSuffix` | string |  |
| `invoice.paidAt` | date |  |
| `invoice.sentAt` | date |  |
| `invoice.sentManually` | boolean |  |
| `invoice.skontoApplied` | boolean |  |
| `invoice.skontoEnabled` | boolean |  |
| `invoice.status` | string |  |
| `invoice.totalAmount` | number |  |
| `invoice.totalNetAmount` | number |  |
| `invoice.type` | string |  |

## Native endpoint

Through the native Mendato API, this operation is `POST /graphql` (base URL `https://api.mendato.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-invoice.md) for the provider-specific parameters and requirements.

