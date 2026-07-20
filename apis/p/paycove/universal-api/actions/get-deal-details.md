# Paycove: Get Deal Details

Retrieves a deal from Paycove.

```
GET https://connect.mindcloud.co/v1/universal/paycove/latest/actions/get-deal-details
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Paycove `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/paycove/latest/actions/get-deal-details?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/paycove/latest/actions/get-deal-details?${params}`, {
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
| `customFieldKeys[]` | array<string> | no | Array of custom field keys to include in the response. |
| `id` | string | yes | Paycove deal id. |
| `scope[]` | array<string> | no | Array of relations to include, such as contact or organization. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "accountId": 1,
      "amountOff": 1,
      "checkoutUrl": "https://example.com",
      "createdAt": "string",
      "crmContactId": "string",
      "crmCreatedAt": {},
      "crmDealId": "string",
      "crmOrganizationId": {},
      "crmStageId": "string",
      "crmUpdatedAt": {},
      "crmUrl": {},
      "currency": "string",
      "daysOverdue": {},
      "dealType": "string",
      "description": {},
      "editLink": "https://example.com",
      "id": 1,
      "invoiceCreatedAt": "string",
      "invoiceCreatedAtFormatted": "string",
      "invoiceDueDate": {},
      "invoiceDueDateFormatted": {},
      "invoicePaid": 1,
      "invoicePaidDate": {},
      "invoiceSentDate": {},
      "invoiceTemplateId": {},
      "isPaid": true,
      "isSent": true,
      "lastChargeCreatedAt": {},
      "lastUpdateFromCrm": {},
      "name": "Ava Chen",
      "paymentsPaid": {},
      "paymentsScheduled": {},
      "paymentsUnpaid": {},
      "pcContactId": "string",
      "pcOrganizationId": {},
      "percentOff": 1,
      "po": "string",
      "previewLink": "https://example.com",
      "quoteAcceptedAt": {},
      "quoteCreatedAt": {},
      "quoteCreatedAtFormatted": {},
      "quoteSent": true,
      "quoteSentDate": {},
      "remainingBalance": 1,
      "signature": {},
      "status": "string",
      "subtotalAmount": 1,
      "totalAmount": "string",
      "totalAmountPaid": {},
      "totalTax": 1,
      "uniqueId": "string",
      "xero": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `accountId` | number |  |
| `amountOff` | number |  |
| `checkoutUrl` | string |  |
| `createdAt` | string |  |
| `crmContactId` | string |  |
| `crmCreatedAt` | object |  |
| `crmDealId` | string |  |
| `crmOrganizationId` | object |  |
| `crmStageId` | string |  |
| `crmUpdatedAt` | object |  |
| `crmUrl` | object |  |
| `currency` | string |  |
| `daysOverdue` | object |  |
| `dealType` | string |  |
| `description` | object |  |
| `editLink` | string |  |
| `id` | number |  |
| `invoiceCreatedAt` | string |  |
| `invoiceCreatedAtFormatted` | string |  |
| `invoiceDueDate` | object |  |
| `invoiceDueDateFormatted` | object |  |
| `invoicePaid` | number |  |
| `invoicePaidDate` | object |  |
| `invoiceSentDate` | object |  |
| `invoiceTemplateId` | object |  |
| `isPaid` | boolean |  |
| `isSent` | boolean |  |
| `lastChargeCreatedAt` | object |  |
| `lastUpdateFromCrm` | object |  |
| `name` | string |  |
| `paymentsPaid` | object |  |
| `paymentsScheduled` | object |  |
| `paymentsUnpaid` | object |  |
| `pcContactId` | string |  |
| `pcOrganizationId` | object |  |
| `percentOff` | number |  |
| `po` | string |  |
| `previewLink` | string |  |
| `quoteAcceptedAt` | object |  |
| `quoteCreatedAt` | object |  |
| `quoteCreatedAtFormatted` | object |  |
| `quoteSent` | boolean |  |
| `quoteSentDate` | object |  |
| `remainingBalance` | number |  |
| `signature` | object |  |
| `status` | string |  |
| `subtotalAmount` | number |  |
| `totalAmount` | string |  |
| `totalAmountPaid` | object |  |
| `totalTax` | number |  |
| `uniqueId` | string |  |
| `xero` | boolean |  |

## Native endpoint

Through the native Paycove API, this operation is `GET deals/:id` (base URL `https://paycove.io/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-deal-details.md) for the provider-specific parameters and requirements.

