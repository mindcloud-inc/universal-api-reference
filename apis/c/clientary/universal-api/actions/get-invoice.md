# Clientary: Get Invoice

Retrieves an invoice from Clientary by invoice ID.

```
GET https://connect.mindcloud.co/v1/universal/clientary/latest/actions/get-invoice
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Clientary `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/clientary/latest/actions/get-invoice?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/clientary/latest/actions/get-invoice?${params}`, {
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
| `id` | string | yes | The Clientary invoice ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "associatedContractId": 1,
      "associatedEstimateId": 1,
      "associatedProjectId": 1,
      "attachmentCurrentPage": 1,
      "attachments": [
        {}
      ],
      "attachmentsEnabled": true,
      "attachmentsRelations": [
        {}
      ],
      "attachmentTotalCount": 1,
      "attachmentTotalPages": 1,
      "balance": 1,
      "client": {
        "id": 1,
        "name": "Ava Chen"
      },
      "clientId": 1,
      "clientViewUrl": "https://example.com",
      "comments": [
        {}
      ],
      "compoundTax": true,
      "createdAt": "2026-05-07T12:00:00.000Z",
      "currencyCode": "string",
      "date": "2026-05-07T12:00:00.000Z",
      "dueDate": "2026-05-07T12:00:00.000Z",
      "externalOrderId": "string",
      "extraFields": {},
      "id": 1,
      "integrationSyncLinks": [
        {}
      ],
      "invoiceItems": [
        {}
      ],
      "lateFeeAmount": 1,
      "lateFeeEnabled": true,
      "lateFeeInterval": 1,
      "nextReminderDate": "2026-05-07T12:00:00.000Z",
      "nonTaxableSubtotal": 1,
      "note": "string",
      "number": "string",
      "paidDate": "2026-05-07T12:00:00.000Z",
      "payments": [
        {}
      ],
      "pendingAmount": 1,
      "po": "string",
      "projects": [
        {}
      ],
      "recipients": [
        {}
      ],
      "recurringAction": "string",
      "recurringEnabled": true,
      "recurringSchedules": [
        {}
      ],
      "recurringTimeInterval": "string",
      "secret": "string",
      "settingsEnablePaymentIntegration": true,
      "settingsEnableProcessingFees": true,
      "shippingAddress": "string",
      "shippingCity": "string",
      "shippingCountry": "string",
      "shippingEnabled": true,
      "shippingName": "Ava Chen",
      "shippingPhone": "string",
      "shippingState": "string",
      "shippingZip": "string",
      "status": 1,
      "subtotal": 1,
      "subtotalLateFees": 1,
      "summary": "string",
      "tax": 1,
      "tax2": 1,
      "tax2Enabled": true,
      "tax2Label": "string",
      "tax3": 1,
      "tax3Label": "string",
      "taxableSubtotal": 1,
      "taxLabel": "string",
      "title": "string",
      "totalCost": 1,
      "totalLateFees": 1,
      "totalPayments": 1,
      "totalTax": 1,
      "totalTax2": 1,
      "totalTax3": 1,
      "totalTaxes": 1,
      "totalTransactionFees": 1,
      "transactionBalance": 1,
      "type": "string",
      "updatedAt": "2026-05-07T12:00:00.000Z",
      "userId": 1,
      "verifactuEstado": "string",
      "verifactuLocked": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `associatedContractId` | number |  |
| `associatedEstimateId` | number |  |
| `associatedProjectId` | number |  |
| `attachmentCurrentPage` | number |  |
| `attachments` | array<object> |  |
| `attachmentsEnabled` | boolean |  |
| `attachmentsRelations` | array<object> |  |
| `attachmentTotalCount` | number |  |
| `attachmentTotalPages` | number |  |
| `balance` | number |  |
| `client.id` | number |  |
| `client.name` | string |  |
| `clientId` | number |  |
| `clientViewUrl` | string |  |
| `comments` | array<object> |  |
| `compoundTax` | boolean |  |
| `createdAt` | date |  |
| `currencyCode` | string |  |
| `date` | date |  |
| `dueDate` | date |  |
| `externalOrderId` | string |  |
| `extraFields` | object |  |
| `id` | number |  |
| `integrationSyncLinks` | array<object> |  |
| `invoiceItems` | array<object> |  |
| `lateFeeAmount` | number |  |
| `lateFeeEnabled` | boolean |  |
| `lateFeeInterval` | number |  |
| `nextReminderDate` | date |  |
| `nonTaxableSubtotal` | number |  |
| `note` | string |  |
| `number` | string |  |
| `paidDate` | date |  |
| `payments` | array<object> |  |
| `pendingAmount` | number |  |
| `po` | string |  |
| `projects` | array<object> |  |
| `recipients` | array<object> |  |
| `recurringAction` | string |  |
| `recurringEnabled` | boolean |  |
| `recurringSchedules` | array<object> |  |
| `recurringTimeInterval` | string |  |
| `secret` | string |  |
| `settingsEnablePaymentIntegration` | boolean |  |
| `settingsEnableProcessingFees` | boolean |  |
| `shippingAddress` | string |  |
| `shippingCity` | string |  |
| `shippingCountry` | string |  |
| `shippingEnabled` | boolean |  |
| `shippingName` | string |  |
| `shippingPhone` | string |  |
| `shippingState` | string |  |
| `shippingZip` | string |  |
| `status` | number |  |
| `subtotal` | number |  |
| `subtotalLateFees` | number |  |
| `summary` | string |  |
| `tax` | number |  |
| `tax2` | number |  |
| `tax2Enabled` | boolean |  |
| `tax2Label` | string |  |
| `tax3` | number |  |
| `tax3Label` | string |  |
| `taxableSubtotal` | number |  |
| `taxLabel` | string |  |
| `title` | string |  |
| `totalCost` | number |  |
| `totalLateFees` | number |  |
| `totalPayments` | number |  |
| `totalTax` | number |  |
| `totalTax2` | number |  |
| `totalTax3` | number |  |
| `totalTaxes` | number |  |
| `totalTransactionFees` | number |  |
| `transactionBalance` | number |  |
| `type` | string |  |
| `updatedAt` | date |  |
| `userId` | number |  |
| `verifactuEstado` | string |  |
| `verifactuLocked` | boolean |  |

## Native endpoint

Through the native Clientary API, this operation is `GET /invoices/:id` (base URL `https://{{credentials.subdomain}}.clientary.com/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-invoice.md) for the provider-specific parameters and requirements.

