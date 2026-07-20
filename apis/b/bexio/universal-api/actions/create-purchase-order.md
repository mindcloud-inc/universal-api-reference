# Bexio: Create Purchase Order

Creates a purchase order in Bexio.

```
POST https://connect.mindcloud.co/v1/universal/bexio/latest/actions/create-purchase-order
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Bexio `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/bexio/latest/actions/create-purchase-order" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/bexio/latest/actions/create-purchase-order', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `documentNr` | string | no |  |
| `kbPaymentTemplateId` | number | no |  |
| `paymentTypeId` | number | no |  |
| `title` | string | no |  |
| `contactId` | number | no |  |
| `contactSubId` | number | no |  |
| `templateSlug` | string | no |  |
| `userId` | number | no |  |
| `projectId` | number | no |  |
| `logopaperId` | number | no |  |
| `languageId` | number | no |  |
| `bankAccountId` | number | no |  |
| `currencyId` | number | no |  |
| `header` | string | no |  |
| `footer` | string | no |  |
| `mwstType` | list<string> | no | One of: `0`, `1`, `2`. |
| `mwstIsNet` | boolean | no |  |
| `isCompactView` | boolean | no |  |
| `showPositionTaxes` | boolean | no |  |
| `salesmanUserId` | number | no |  |
| `isValidFrom` | date | no |  |
| `isValidTo` | date | no |  |
| `deliveryAddressType` | list<string> | no | One of: `0`, `1`. |
| `contactAddressManual` | string | no |  |
| `deliveryAddressManual` | string | no |  |
| `nbDecimalsAmount` | number | no |  |
| `nbDecimalsPrice` | number | no |  |
| `termsOfPaymentText` | string | no |  |
| `reference` | string | no |  |
| `apiReference` | string | no |  |
| `mail` | string | no |  |
| `positions` | object | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "apiReference": {},
      "bankAccountId": 1,
      "contactAddressManual": "string",
      "contactId": 1,
      "contactSubId": {},
      "createdAt": "2026-05-07T12:00:00.000Z",
      "currencyId": 1,
      "customTranslations": {
        "addedMwst": "string",
        "articleProductcode": "string",
        "cancelled": "string",
        "cashDiscount": "string",
        "colHeaderAccountStatementPrice": "string",
        "colHeaderAmount": "string",
        "colHeaderAmountDelivered": "string",
        "colHeaderAmountLeft": "string",
        "colHeaderAmountRequested": "string",
        "colHeaderDate": "string",
        "colHeaderDescription": "string",
        "colHeaderDiscount": "string",
        "colHeaderDocumentNr": "string",
        "colHeaderDue": "string",
        "colHeaderPickingSlipAmount": "string",
        "colHeaderPickingSlipRemarks": "string",
        "colHeaderPos": "string",
        "colHeaderPriceLeftForPayment": "string",
        "colHeaderReminderLevel": "string",
        "colHeaderSinglePrice": "string",
        "colHeaderStock": "string",
        "colHeaderStockPlace": "string",
        "colHeaderText": "string",
        "colHeaderTotalPrice": "string",
        "colHeaderUnit": "string",
        "companyProfileMwstNr": "string",
        "conditionsOfPayment": "string",
        "includedMwst": "string",
        "itemInfoAccomplishmentDate": "string",
        "itemInfoClientNr": "string",
        "itemInfoCreditVoucherNr": "string",
        "itemInfoDate": "string",
        "itemInfoDeliverableUntil": "string",
        "itemInfoDeliveryAddress": "string",
        "itemInfoDeliverySlipNr": "string",
        "itemInfoInvoicableUntil": "string",
        "itemInfoInvoiceDate": "string",
        "itemInfoInvoiceNr": "string",
        "itemInfoOrderNr": "string",
        "itemInfoProjectNr": "string",
        "itemInfoReference": "string",
        "itemInfoUser": "string",
        "itemInfoUstNr": "string",
        "itemInfoValidUntil": "string",
        "kbAccountStatementBalance": "string",
        "kbAccountStatementBalanceInFavorOfClient": "string",
        "kbAccountStatementBalanceInFavorOfContact": "string",
        "kbAccountStatementBalanceTotalInFavorOfClient": "string",
        "kbAccountStatementBalanceTotalInFavorOfContact": "string",
        "kbAccountStatementTitle": "string",
        "kbArticleOrderDelivererCode": "string",
        "kbArticleOrderDelivererNr": "string",
        "kbArticleOrderTitle": "string",
        "kbArticleOrderTotalMwstExcluded": "string",
        "kbArticleOrderTotalMwstExempt": "string",
        "kbArticleOrderTotalMwstIncluded": "string",
        "kbBillTitle": "string",
        "kbBilltotalMwstExcluded": "string",
        "kbBillTotalMwstExempt": "string",
        "kbBillTotalMwstIncluded": "string",
        "kbCreditVoucherTitle": "string",
        "kbCreditVoucherTotalMwstExcluded": "string",
        "kbCreditVoucherTotalMwstExempt": "string",
        "kbCreditVoucherTotalMwstIncluded": "string",
        "kbDeliveryTitle": "string",
        "kbInvoiceClientAccountRedemption": "string",
        "kbInvoiceReceiptOfCashDiscount": "string",
        "kbInvoiceReceiptOfOverpayment": "string",
        "kbInvoiceReceiptOfPayment": "string",
        "kbInvoiceTitle": "string",
        "kbInvoiceTotalMwstExcluded": "string",
        "kbInvoiceTotalMwstExempt": "string",
        "kbInvoiceTotalMwstIncluded": "string",
        "kbOfferTitle": "string",
        "kbOfferTotalMwstExcluded": "string",
        "kbOfferTotalMwstExempt": "string",
        "kbOfferTotalMwstIncluded": "string",
        "kbOrderDeliveryAddress": "string",
        "kbOrderTitle": "string",
        "kbOrderTotalMwstExcluded": "string",
        "kbOrderTotalMwstExempt": "string",
        "kbOrderTotalMwstIncluded": "string",
        "kbPickingSlipTitle": "string",
        "kbPositionItemTotalPaymentEntryCredit": "string",
        "kbPositionItemTotalPaymentEntryPayment": "string",
        "optionalPositions": "string",
        "pageXOfY": "string",
        "partBillDescription": "string",
        "paymentTimePeriod": "string",
        "payNow": "string",
        "positionImportExpenseDate": "string",
        "positionImportMonitoringDate": "string",
        "positionImportProject": "string",
        "receivedPayments": "string",
        "remainingAmount": "string",
        "rounding": "string",
        "subTotal": "string",
        "total": "string"
      },
      "dateFormat": {
        "dateFormat": "string",
        "dateFormatId": 1
      },
      "deliveryAddressManual": "string",
      "deliveryAddressType": "string",
      "documentNr": "string",
      "footer": "string",
      "header": "string",
      "id": 1,
      "isCompactView": true,
      "isValidFrom": "2026-05-07T12:00:00.000Z",
      "isValidTo": "2026-05-07T12:00:00.000Z",
      "isValidUntil": "2026-05-07T12:00:00.000Z",
      "kbItemStatusId": 1,
      "kbPaymentTemplateId": {},
      "languageId": 1,
      "logopaperId": 1,
      "mail": {},
      "mwstIsNet": true,
      "mwstType": "string",
      "nbDecimalsAmount": 1,
      "nbDecimalsPrice": 1,
      "paymentTypeId": 1,
      "positions": {
        "total": 1,
        "totalDiscount": 1,
        "totalGross": 1,
        "totalNet": 1,
        "totalTax": 1
      },
      "projectId": {},
      "reference": {},
      "salesmanUserId": {},
      "showPositionTaxes": true,
      "templateSlug": "string",
      "termsOfPaymentText": {},
      "title": "string",
      "totalRoundingDifference": 1,
      "updatedAt": "2026-05-07T12:00:00.000Z",
      "userId": 1,
      "viewedByClientAt": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `apiReference` | object |  |
| `bankAccountId` | number |  |
| `contactAddressManual` | string |  |
| `contactId` | number |  |
| `contactSubId` | object |  |
| `createdAt` | date |  |
| `currencyId` | number |  |
| `customTranslations.addedMwst` | string |  |
| `customTranslations.articleProductcode` | string |  |
| `customTranslations.cancelled` | string |  |
| `customTranslations.cashDiscount` | string |  |
| `customTranslations.colHeaderAccountStatementPrice` | string |  |
| `customTranslations.colHeaderAmount` | string |  |
| `customTranslations.colHeaderAmountDelivered` | string |  |
| `customTranslations.colHeaderAmountLeft` | string |  |
| `customTranslations.colHeaderAmountRequested` | string |  |
| `customTranslations.colHeaderDate` | string |  |
| `customTranslations.colHeaderDescription` | string |  |
| `customTranslations.colHeaderDiscount` | string |  |
| `customTranslations.colHeaderDocumentNr` | string |  |
| `customTranslations.colHeaderDue` | string |  |
| `customTranslations.colHeaderPickingSlipAmount` | string |  |
| `customTranslations.colHeaderPickingSlipRemarks` | string |  |
| `customTranslations.colHeaderPos` | string |  |
| `customTranslations.colHeaderPriceLeftForPayment` | string |  |
| `customTranslations.colHeaderReminderLevel` | string |  |
| `customTranslations.colHeaderSinglePrice` | string |  |
| `customTranslations.colHeaderStock` | string |  |
| `customTranslations.colHeaderStockPlace` | string |  |
| `customTranslations.colHeaderText` | string |  |
| `customTranslations.colHeaderTotalPrice` | string |  |
| `customTranslations.colHeaderUnit` | string |  |
| `customTranslations.companyProfileMwstNr` | string |  |
| `customTranslations.conditionsOfPayment` | string |  |
| `customTranslations.includedMwst` | string |  |
| `customTranslations.itemInfoAccomplishmentDate` | string |  |
| `customTranslations.itemInfoClientNr` | string |  |
| `customTranslations.itemInfoCreditVoucherNr` | string |  |
| `customTranslations.itemInfoDate` | string |  |
| `customTranslations.itemInfoDeliverableUntil` | string |  |
| `customTranslations.itemInfoDeliveryAddress` | string |  |
| `customTranslations.itemInfoDeliverySlipNr` | string |  |
| `customTranslations.itemInfoInvoicableUntil` | string |  |
| `customTranslations.itemInfoInvoiceDate` | string |  |
| `customTranslations.itemInfoInvoiceNr` | string |  |
| `customTranslations.itemInfoOrderNr` | string |  |
| `customTranslations.itemInfoProjectNr` | string |  |
| `customTranslations.itemInfoReference` | string |  |
| `customTranslations.itemInfoUser` | string |  |
| `customTranslations.itemInfoUstNr` | string |  |
| `customTranslations.itemInfoValidUntil` | string |  |
| `customTranslations.kbAccountStatementBalance` | string |  |
| `customTranslations.kbAccountStatementBalanceInFavorOfClient` | string |  |
| `customTranslations.kbAccountStatementBalanceInFavorOfContact` | string |  |
| `customTranslations.kbAccountStatementBalanceTotalInFavorOfClient` | string |  |
| `customTranslations.kbAccountStatementBalanceTotalInFavorOfContact` | string |  |
| `customTranslations.kbAccountStatementTitle` | string |  |
| `customTranslations.kbArticleOrderDelivererCode` | string |  |
| `customTranslations.kbArticleOrderDelivererNr` | string |  |
| `customTranslations.kbArticleOrderTitle` | string |  |
| `customTranslations.kbArticleOrderTotalMwstExcluded` | string |  |
| `customTranslations.kbArticleOrderTotalMwstExempt` | string |  |
| `customTranslations.kbArticleOrderTotalMwstIncluded` | string |  |
| `customTranslations.kbBillTitle` | string |  |
| `customTranslations.kbBilltotalMwstExcluded` | string |  |
| `customTranslations.kbBillTotalMwstExempt` | string |  |
| `customTranslations.kbBillTotalMwstIncluded` | string |  |
| `customTranslations.kbCreditVoucherTitle` | string |  |
| `customTranslations.kbCreditVoucherTotalMwstExcluded` | string |  |
| `customTranslations.kbCreditVoucherTotalMwstExempt` | string |  |
| `customTranslations.kbCreditVoucherTotalMwstIncluded` | string |  |
| `customTranslations.kbDeliveryTitle` | string |  |
| `customTranslations.kbInvoiceClientAccountRedemption` | string |  |
| `customTranslations.kbInvoiceReceiptOfCashDiscount` | string |  |
| `customTranslations.kbInvoiceReceiptOfOverpayment` | string |  |
| `customTranslations.kbInvoiceReceiptOfPayment` | string |  |
| `customTranslations.kbInvoiceTitle` | string |  |
| `customTranslations.kbInvoiceTotalMwstExcluded` | string |  |
| `customTranslations.kbInvoiceTotalMwstExempt` | string |  |
| `customTranslations.kbInvoiceTotalMwstIncluded` | string |  |
| `customTranslations.kbOfferTitle` | string |  |
| `customTranslations.kbOfferTotalMwstExcluded` | string |  |
| `customTranslations.kbOfferTotalMwstExempt` | string |  |
| `customTranslations.kbOfferTotalMwstIncluded` | string |  |
| `customTranslations.kbOrderDeliveryAddress` | string |  |
| `customTranslations.kbOrderTitle` | string |  |
| `customTranslations.kbOrderTotalMwstExcluded` | string |  |
| `customTranslations.kbOrderTotalMwstExempt` | string |  |
| `customTranslations.kbOrderTotalMwstIncluded` | string |  |
| `customTranslations.kbPickingSlipTitle` | string |  |
| `customTranslations.kbPositionItemTotalPaymentEntryCredit` | string |  |
| `customTranslations.kbPositionItemTotalPaymentEntryPayment` | string |  |
| `customTranslations.optionalPositions` | string |  |
| `customTranslations.pageXOfY` | string |  |
| `customTranslations.partBillDescription` | string |  |
| `customTranslations.paymentTimePeriod` | string |  |
| `customTranslations.payNow` | string |  |
| `customTranslations.positionImportExpenseDate` | string |  |
| `customTranslations.positionImportMonitoringDate` | string |  |
| `customTranslations.positionImportProject` | string |  |
| `customTranslations.receivedPayments` | string |  |
| `customTranslations.remainingAmount` | string |  |
| `customTranslations.rounding` | string |  |
| `customTranslations.subTotal` | string |  |
| `customTranslations.total` | string |  |
| `dateFormat.dateFormat` | string |  |
| `dateFormat.dateFormatId` | number |  |
| `deliveryAddressManual` | string |  |
| `deliveryAddressType` | string |  |
| `documentNr` | string |  |
| `footer` | string |  |
| `header` | string |  |
| `id` | number |  |
| `isCompactView` | boolean |  |
| `isValidFrom` | date |  |
| `isValidTo` | date |  |
| `isValidUntil` | date |  |
| `kbItemStatusId` | number |  |
| `kbPaymentTemplateId` | object |  |
| `languageId` | number |  |
| `logopaperId` | number |  |
| `mail` | object |  |
| `mwstIsNet` | boolean |  |
| `mwstType` | string |  |
| `nbDecimalsAmount` | number |  |
| `nbDecimalsPrice` | number |  |
| `paymentTypeId` | number |  |
| `positions.total` | number |  |
| `positions.totalDiscount` | number |  |
| `positions.totalGross` | number |  |
| `positions.totalNet` | number |  |
| `positions.totalTax` | number |  |
| `projectId` | object |  |
| `reference` | object |  |
| `salesmanUserId` | object |  |
| `showPositionTaxes` | boolean |  |
| `templateSlug` | string |  |
| `termsOfPaymentText` | object |  |
| `title` | string |  |
| `totalRoundingDifference` | number |  |
| `updatedAt` | date |  |
| `userId` | number |  |
| `viewedByClientAt` | date |  |

## Native endpoint

Through the native Bexio API, this operation is `POST /3.0/purchase_orders` (base URL `https://api.bexio.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-purchase-order.md) for the provider-specific parameters and requirements.

