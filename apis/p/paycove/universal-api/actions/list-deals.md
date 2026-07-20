# Paycove: List Deals

Retrieves deals from Paycove.

```
GET https://connect.mindcloud.co/v1/universal/paycove/latest/actions/list-deals
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Paycove `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/paycove/latest/actions/list-deals?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/paycove/latest/actions/list-deals?${params}`, {
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
| `includePayments` | boolean | no | Include nested payments in the response. |

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
      "crmContactId": {},
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
      "invoiceCreatedAt": {},
      "invoiceDueDate": {},
      "invoicePaid": 1,
      "invoicePaidDate": {},
      "invoiceSentDate": {},
      "invoiceTemplateId": {},
      "lastUpdateFromCrm": {},
      "name": "Ava Chen",
      "payments": {},
      "paymentsPaid": {},
      "paymentsScheduled": {},
      "paymentsUnpaid": {},
      "pcContactId": {},
      "pcOrganizationId": {},
      "percentOff": 1,
      "po": "string",
      "quoteAcceptedAt": {},
      "quoteCreatedAt": "string",
      "quoteSentDate": {},
      "remainingBalance": {},
      "signature": {},
      "state": {},
      "status": "string",
      "subtotalAmount": {},
      "totalAmount": "string",
      "totalAmountPaid": {},
      "uniqueId": "string",
      "updatedAt": {}
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
| `crmContactId` | object |  |
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
| `invoiceCreatedAt` | object |  |
| `invoiceDueDate` | object |  |
| `invoicePaid` | number |  |
| `invoicePaidDate` | object |  |
| `invoiceSentDate` | object |  |
| `invoiceTemplateId` | object |  |
| `lastUpdateFromCrm` | object |  |
| `name` | string |  |
| `payments` | object |  |
| `paymentsPaid` | object |  |
| `paymentsScheduled` | object |  |
| `paymentsUnpaid` | object |  |
| `pcContactId` | object |  |
| `pcOrganizationId` | object |  |
| `percentOff` | number |  |
| `po` | string |  |
| `quoteAcceptedAt` | object |  |
| `quoteCreatedAt` | string |  |
| `quoteSentDate` | object |  |
| `remainingBalance` | object |  |
| `signature` | object |  |
| `state` | object |  |
| `status` | string |  |
| `subtotalAmount` | object |  |
| `totalAmount` | string |  |
| `totalAmountPaid` | object |  |
| `uniqueId` | string |  |
| `updatedAt` | object |  |

## Native endpoint

Through the native Paycove API, this operation is `GET deals` (base URL `https://paycove.io/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-deals.md) for the provider-specific parameters and requirements.

