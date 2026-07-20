# Paycove: Reassign To New CRM Deal

Updates a Paycove deal with a new CRM deal ID.

```
PUT https://connect.mindcloud.co/v1/universal/paycove/latest/actions/reassign-to-new-crm-deal
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Paycove `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/paycove/latest/actions/reassign-to-new-crm-deal" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "crmDealId": "string",
  "id": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/paycove/latest/actions/reassign-to-new-crm-deal', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "crmDealId": "string",
    "id": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `crmDealId` | string | yes | New CRM deal id to assign. |
| `id` | string | yes | Paycove deal id. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "amountOff": 1,
      "bccRecipients": {},
      "ccRecipients": {},
      "commission": {},
      "contactId": "string",
      "countryCode": {},
      "couponId": {},
      "coverLetter": {},
      "createdAt": "string",
      "creatorId": {},
      "crm": "string",
      "crmCreatedAt": {},
      "crmDealId": "string",
      "crmFiles": {},
      "crmStatus": {},
      "crmUpdatedAt": {},
      "csvExportedAt": {},
      "currency": "string",
      "customerPoFileUrl": {},
      "customerPoNumber": {},
      "customerPoUpdated": {},
      "customFieldTaxes": {},
      "customInvoiceNum": {},
      "customQuoteNum": {},
      "dbAmountPaid": {},
      "dbCommissionAmount": {},
      "dbCrmUrl": {},
      "dbDueDate": {},
      "dbInvoiceFirstSent": {},
      "dbInvoiceSent": {},
      "dbLastPaymentPaid": {},
      "dbPaymentsNotOverdue": {},
      "dbPaymentsOverdue": {},
      "dbPaymentsPaid": {},
      "dbPaymentsScheduled": {},
      "dbPaymentsUnpaid": {},
      "dbPo": "string",
      "dbProfit": {},
      "dbQuoteFirstSent": {},
      "dbQuoteSent": {},
      "dbRemainingBalance": 1,
      "dbStatus": "string",
      "dbSubtotal": 1,
      "dbTotal": 1,
      "dbType": "string",
      "dbVendorCosts": {},
      "dealCustomization": {},
      "deletedAt": {},
      "description": {},
      "dueDateManual": {},
      "footer": {},
      "gateway": {},
      "headerAccount": {},
      "headerCustomer": {},
      "hot": {},
      "id": 1,
      "ideaRoomId": {},
      "incrementId": 1,
      "incrementQuoteId": 1,
      "infoDetails": {},
      "infoDetailsLabel": {},
      "invNotes": {},
      "invoiceCreatedAt": "string",
      "invoiceDueDateFrom": {},
      "invoiceDueInDays": {},
      "invoicePaid": 1,
      "invoicePaidDate": {},
      "invoicePdf": {},
      "invoiceTemplateId": {},
      "invoiceTerms": {},
      "invPaymentTerms": {},
      "invPaymentTermsLabel": {},
      "lastUpdateFromCrm": {},
      "lineItemColumns": {},
      "lineItemColumnsOrder": {},
      "name": "Ava Chen",
      "normalizedValue": 1,
      "notesHistory": {},
      "notesLabel": {},
      "order": {},
      "organizationId": "string",
      "ownerId": {},
      "packageDetails": {},
      "packageDetailsLabel": {},
      "pcContactId": "string",
      "pcCreatorId": 1,
      "pcOrderId": {},
      "pcOrderItemId": {},
      "pcOrganizationId": "string",
      "pcOrgId": {},
      "pcStageId": "string",
      "pcUserId": {},
      "percentOff": 1,
      "primaryDealId": {},
      "productsLabel": {},
      "quoteAcceptedAt": {},
      "quoteAcceptedPdf": {},
      "quoteCreatedAt": {},
      "quotePdf": {},
      "recurringChargeColumns": {},
      "recurringChargeColumnsOrder": {},
      "recurringChargesLabel": {},
      "referenceNum": {},
      "requiresSignature": 1,
      "scheduledColumns": {},
      "scheduledLabelsOrder": {},
      "scheduledPaymentsLabel": {},
      "sendReminders": 1,
      "sentViaWebhookAt": {},
      "serviceFees": 1,
      "signatory": {},
      "sourceId": {},
      "stageId": "string",
      "state": "string",
      "subtotal": 1,
      "taxRate": 1,
      "taxSummary": {},
      "tos": {},
      "uniqueId": "string",
      "updatedAt": "string",
      "value": 1,
      "vatNumber": {},
      "vatTax": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `amountOff` | number |  |
| `bccRecipients` | object |  |
| `ccRecipients` | object |  |
| `commission` | object |  |
| `contactId` | string |  |
| `countryCode` | object |  |
| `couponId` | object |  |
| `coverLetter` | object |  |
| `createdAt` | string |  |
| `creatorId` | object |  |
| `crm` | string |  |
| `crmCreatedAt` | object |  |
| `crmDealId` | string |  |
| `crmFiles` | object |  |
| `crmStatus` | object |  |
| `crmUpdatedAt` | object |  |
| `csvExportedAt` | object |  |
| `currency` | string |  |
| `customerPoFileUrl` | object |  |
| `customerPoNumber` | object |  |
| `customerPoUpdated` | object |  |
| `customFieldTaxes` | object |  |
| `customInvoiceNum` | object |  |
| `customQuoteNum` | object |  |
| `dbAmountPaid` | object |  |
| `dbCommissionAmount` | object |  |
| `dbCrmUrl` | object |  |
| `dbDueDate` | object |  |
| `dbInvoiceFirstSent` | object |  |
| `dbInvoiceSent` | object |  |
| `dbLastPaymentPaid` | object |  |
| `dbPaymentsNotOverdue` | object |  |
| `dbPaymentsOverdue` | object |  |
| `dbPaymentsPaid` | object |  |
| `dbPaymentsScheduled` | object |  |
| `dbPaymentsUnpaid` | object |  |
| `dbPo` | string |  |
| `dbProfit` | object |  |
| `dbQuoteFirstSent` | object |  |
| `dbQuoteSent` | object |  |
| `dbRemainingBalance` | number |  |
| `dbStatus` | string |  |
| `dbSubtotal` | number |  |
| `dbTotal` | number |  |
| `dbType` | string |  |
| `dbVendorCosts` | object |  |
| `dealCustomization` | object |  |
| `deletedAt` | object |  |
| `description` | object |  |
| `dueDateManual` | object |  |
| `footer` | object |  |
| `gateway` | object |  |
| `headerAccount` | object |  |
| `headerCustomer` | object |  |
| `hot` | object |  |
| `id` | number |  |
| `ideaRoomId` | object |  |
| `incrementId` | number |  |
| `incrementQuoteId` | number |  |
| `infoDetails` | object |  |
| `infoDetailsLabel` | object |  |
| `invNotes` | object |  |
| `invoiceCreatedAt` | string |  |
| `invoiceDueDateFrom` | object |  |
| `invoiceDueInDays` | object |  |
| `invoicePaid` | number |  |
| `invoicePaidDate` | object |  |
| `invoicePdf` | object |  |
| `invoiceTemplateId` | object |  |
| `invoiceTerms` | object |  |
| `invPaymentTerms` | object |  |
| `invPaymentTermsLabel` | object |  |
| `lastUpdateFromCrm` | object |  |
| `lineItemColumns` | object |  |
| `lineItemColumnsOrder` | object |  |
| `name` | string |  |
| `normalizedValue` | number |  |
| `notesHistory` | object |  |
| `notesLabel` | object |  |
| `order` | object |  |
| `organizationId` | string |  |
| `ownerId` | object |  |
| `packageDetails` | object |  |
| `packageDetailsLabel` | object |  |
| `pcContactId` | string |  |
| `pcCreatorId` | number |  |
| `pcOrderId` | object |  |
| `pcOrderItemId` | object |  |
| `pcOrganizationId` | string |  |
| `pcOrgId` | object |  |
| `pcStageId` | string |  |
| `pcUserId` | object |  |
| `percentOff` | number |  |
| `primaryDealId` | object |  |
| `productsLabel` | object |  |
| `quoteAcceptedAt` | object |  |
| `quoteAcceptedPdf` | object |  |
| `quoteCreatedAt` | object |  |
| `quotePdf` | object |  |
| `recurringChargeColumns` | object |  |
| `recurringChargeColumnsOrder` | object |  |
| `recurringChargesLabel` | object |  |
| `referenceNum` | object |  |
| `requiresSignature` | number |  |
| `scheduledColumns` | object |  |
| `scheduledLabelsOrder` | object |  |
| `scheduledPaymentsLabel` | object |  |
| `sendReminders` | number |  |
| `sentViaWebhookAt` | object |  |
| `serviceFees` | number |  |
| `signatory` | object |  |
| `sourceId` | object |  |
| `stageId` | string |  |
| `state` | string |  |
| `subtotal` | number |  |
| `taxRate` | number |  |
| `taxSummary` | object |  |
| `tos` | object |  |
| `uniqueId` | string |  |
| `updatedAt` | string |  |
| `value` | number |  |
| `vatNumber` | object |  |
| `vatTax` | number |  |

## Native endpoint

Through the native Paycove API, this operation is `PATCH deals/:id/update-crm-deal-id` (base URL `https://paycove.io/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/reassign-to-new-crm-deal.md) for the provider-specific parameters and requirements.

