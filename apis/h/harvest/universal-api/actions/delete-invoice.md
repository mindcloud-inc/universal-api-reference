# Harvest: Delete invoice

Deletes an existing invoice from Harvest.

```
DELETE https://connect.mindcloud.co/v1/universal/harvest/latest/actions/delete-invoice
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Harvest `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/harvest/latest/actions/delete-invoice?connectionId=$CONNECTION_ID&id=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/harvest/latest/actions/delete-invoice?${params}`, {
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
| `id` | number | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "amount": 1,
      "client": {},
      "clientKey": "string",
      "closedAt": "2026-05-07T12:00:00.000Z",
      "createdAt": "2026-05-07T12:00:00.000Z",
      "creator": {},
      "currency": "string",
      "discount": 1,
      "discountAmount": 1,
      "dueAmount": 1,
      "dueDate": "2026-05-07T12:00:00.000Z",
      "estimate": {},
      "id": 1,
      "issueDate": "2026-05-07T12:00:00.000Z",
      "lineItems": [
        {}
      ],
      "notes": "string",
      "number": "string",
      "paidAt": "2026-05-07T12:00:00.000Z",
      "paidDate": "2026-05-07T12:00:00.000Z",
      "paymentOptions": [
        "string"
      ],
      "paymentTerm": "string",
      "periodEnd": "2026-05-07T12:00:00.000Z",
      "periodStart": "2026-05-07T12:00:00.000Z",
      "purchaseOrder": "string",
      "recurringInvoiceId": 1,
      "retainer": {},
      "sentAt": "2026-05-07T12:00:00.000Z",
      "state": "string",
      "subject": "string",
      "tax": 1,
      "tax2": 1,
      "tax2Amount": 1,
      "taxAmount": 1,
      "updatedAt": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `amount` | number |  |
| `client` | object |  |
| `clientKey` | string |  |
| `closedAt` | date |  |
| `createdAt` | date |  |
| `creator` | object |  |
| `currency` | string |  |
| `discount` | number |  |
| `discountAmount` | number |  |
| `dueAmount` | number |  |
| `dueDate` | date |  |
| `estimate` | object |  |
| `id` | number |  |
| `issueDate` | date |  |
| `lineItems` | array<object> |  |
| `notes` | string |  |
| `number` | string |  |
| `paidAt` | date |  |
| `paidDate` | date |  |
| `paymentOptions` | array<string> |  |
| `paymentTerm` | string |  |
| `periodEnd` | date |  |
| `periodStart` | date |  |
| `purchaseOrder` | string |  |
| `recurringInvoiceId` | number |  |
| `retainer` | object |  |
| `sentAt` | date |  |
| `state` | string |  |
| `subject` | string |  |
| `tax` | number |  |
| `tax2` | number |  |
| `tax2Amount` | number |  |
| `taxAmount` | number |  |
| `updatedAt` | date |  |

## Native endpoint

Through the native Harvest API, this operation is `DELETE /v2/invoices/:id` (base URL `https://api.harvestapp.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-invoice.md) for the provider-specific parameters and requirements.

