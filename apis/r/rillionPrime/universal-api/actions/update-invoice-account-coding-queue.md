# Rillion Prime: Update Invoice Account Coding Queue



```
PUT https://connect.mindcloud.co/v1/universal/rillionPrime/latest/actions/update-invoice-account-coding-queue
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Rillion Prime `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/rillionPrime/latest/actions/update-invoice-account-coding-queue" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "invoiceAccountCodingQueueId": 1,
  "invoiceQueueId": 1,
  "type": "string",
  "createUser": "string",
  "createRole": "string",
  "signUser": "string",
  "signRole": "string",
  "acceptUser": "string",
  "acceptRole": "string",
  "account": "string",
  "object1": "string",
  "object2": "string",
  "object3": "string",
  "object4": "string",
  "object5": "string",
  "object6": "string",
  "object7": "string",
  "object8": "string",
  "currency": "string",
  "amount": 1,
  "baseAmount": 1,
  "number": 1,
  "vatCode": "string",
  "vatDeduction": 1,
  "allocationsAccount": "string",
  "allocateFromDate": "2026-05-07T12:00:00.000Z",
  "allocateToDate": "2026-05-07T12:00:00.000Z",
  "forwardInvoice": "string",
  "assetType": "string",
  "assetName": "Ava Chen",
  "assetDescription": "string",
  "assetDate": "2026-05-07T12:00:00.000Z",
  "ownerAsset": "string",
  "purchaseOrderNo": "string",
  "purchaseOrderLineNo": "string",
  "note": "string",
  "group1": "string",
  "group2": "string",
  "group3": "string",
  "group4": "string",
  "group5": "string",
  "group6": "string",
  "invoiceAccountCodingLineNo": 1,
  "allocationType": "string",
  "lineVatAmount": 1,
  "vatCalculationRule": "string",
  "purchaseOrderLineId": 1,
  "queueType": 1,
  "queueStatus": 1,
  "errorText": "string",
  "invoiceAccountCodingId": 1,
  "rowIndex": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/rillionPrime/latest/actions/update-invoice-account-coding-queue', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "invoiceAccountCodingQueueId": 1,
    "invoiceQueueId": 1,
    "type": "string",
    "createUser": "string",
    "createRole": "string",
    "signUser": "string",
    "signRole": "string",
    "acceptUser": "string",
    "acceptRole": "string",
    "account": "string",
    "object1": "string",
    "object2": "string",
    "object3": "string",
    "object4": "string",
    "object5": "string",
    "object6": "string",
    "object7": "string",
    "object8": "string",
    "currency": "string",
    "amount": 1,
    "baseAmount": 1,
    "number": 1,
    "vatCode": "string",
    "vatDeduction": 1,
    "allocationsAccount": "string",
    "allocateFromDate": "2026-05-07T12:00:00.000Z",
    "allocateToDate": "2026-05-07T12:00:00.000Z",
    "forwardInvoice": "string",
    "assetType": "string",
    "assetName": "Ava Chen",
    "assetDescription": "string",
    "assetDate": "2026-05-07T12:00:00.000Z",
    "ownerAsset": "string",
    "purchaseOrderNo": "string",
    "purchaseOrderLineNo": "string",
    "note": "string",
    "group1": "string",
    "group2": "string",
    "group3": "string",
    "group4": "string",
    "group5": "string",
    "group6": "string",
    "invoiceAccountCodingLineNo": 1,
    "allocationType": "string",
    "lineVatAmount": 1,
    "vatCalculationRule": "string",
    "purchaseOrderLineId": 1,
    "queueType": 1,
    "queueStatus": 1,
    "errorText": "string",
    "invoiceAccountCodingId": 1,
    "rowIndex": 1,
    "invoiceQueueId": 1,
    "type": "string",
    "createUser": "string",
    "createRole": "string",
    "signUser": "string",
    "signRole": "string",
    "acceptUser": "string",
    "acceptRole": "string",
    "account": "string",
    "object1": "string",
    "object2": "string",
    "object3": "string",
    "object4": "string",
    "object5": "string",
    "object6": "string",
    "object7": "string",
    "object8": "string",
    "currency": "string",
    "amount": 1,
    "baseAmount": 1,
    "number": 1,
    "vatCode": "string",
    "vatDeduction": 1,
    "allocationsAccount": "string",
    "allocateFromDate": "2026-05-07T12:00:00.000Z",
    "allocateToDate": "2026-05-07T12:00:00.000Z",
    "forwardInvoice": "string",
    "assetType": "string",
    "assetName": "Ava Chen",
    "assetDescription": "string",
    "assetDate": "2026-05-07T12:00:00.000Z",
    "ownerAsset": "string",
    "purchaseOrderNo": "string",
    "purchaseOrderLineNo": "string",
    "note": "string",
    "group1": "string",
    "group2": "string",
    "group3": "string",
    "group4": "string",
    "group5": "string",
    "group6": "string",
    "invoiceAccountCodingLineNo": 1,
    "allocationType": "string",
    "lineVatAmount": 1,
    "vatCalculationRule": "string",
    "purchaseOrderLineId": 1,
    "queueType": 1,
    "queueStatus": 1,
    "errorText": "string",
    "invoiceAccountCodingId": 1,
    "rowIndex": 1,
    "invoiceQueueId": 1,
    "type": "string",
    "createUser": "string",
    "createRole": "string",
    "signUser": "string",
    "signRole": "string",
    "acceptUser": "string",
    "acceptRole": "string",
    "account": "string",
    "object1": "string",
    "object2": "string",
    "object3": "string",
    "object4": "string",
    "object5": "string",
    "object6": "string",
    "object7": "string",
    "object8": "string",
    "currency": "string",
    "amount": 1,
    "baseAmount": 1,
    "number": 1,
    "vatCode": "string",
    "vatDeduction": 1,
    "allocationsAccount": "string",
    "allocateFromDate": "2026-05-07T12:00:00.000Z",
    "allocateToDate": "2026-05-07T12:00:00.000Z",
    "forwardInvoice": "string",
    "assetType": "string",
    "assetName": "Ava Chen",
    "assetDescription": "string",
    "assetDate": "2026-05-07T12:00:00.000Z",
    "ownerAsset": "string",
    "purchaseOrderNo": "string",
    "purchaseOrderLineNo": "string",
    "note": "string",
    "group1": "string",
    "group2": "string",
    "group3": "string",
    "group4": "string",
    "group5": "string",
    "group6": "string",
    "invoiceAccountCodingLineNo": 1,
    "allocationType": "string",
    "lineVatAmount": 1,
    "vatCalculationRule": "string",
    "purchaseOrderLineId": 1,
    "queueType": 1,
    "queueStatus": 1,
    "errorText": "string",
    "invoiceAccountCodingId": 1,
    "rowIndex": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `invoiceAccountCodingQueueId` | number | yes | Path value for InvoiceAccountCodingQueueId. |
| `invoiceQueueId` | number | yes | Request body value for InvoiceQueueId. |
| `type` | string | yes | Request body value for Type. |
| `createUser` | string | yes | Request body value for CreateUser. |
| `createRole` | string | yes | Request body value for CreateRole. |
| `signUser` | string | yes | Request body value for SignUser. |
| `signRole` | string | yes | Request body value for SignRole. |
| `acceptUser` | string | yes | Request body value for AcceptUser. |
| `acceptRole` | string | yes | Request body value for AcceptRole. |
| `account` | string | yes | Request body value for Account. |
| `object1` | string | yes | Request body value for Object1. |
| `object2` | string | yes | Request body value for Object2. |
| `object3` | string | yes | Request body value for Object3. |
| `object4` | string | yes | Request body value for Object4. |
| `object5` | string | yes | Request body value for Object5. |
| `object6` | string | yes | Request body value for Object6. |
| `object7` | string | yes | Request body value for Object7. |
| `object8` | string | yes | Request body value for Object8. |
| `currency` | string | yes | Request body value for Currency. |
| `amount` | number | yes | Request body value for Amount. |
| `baseAmount` | number | yes | Request body value for BaseAmount. |
| `number` | number | yes | Request body value for Number. |
| `vatCode` | string | yes | Request body value for VatCode. |
| `vatDeduction` | number | yes | Request body value for VatDeduction. |
| `allocationsAccount` | string | yes | Request body value for AllocationsAccount. |
| `allocateFromDate` | date | yes | Request body value for AllocateFromDate. |
| `allocateToDate` | date | yes | Request body value for AllocateToDate. |
| `forwardInvoice` | string | yes | Request body value for ForwardInvoice. |
| `assetType` | string | yes | Request body value for AssetType. |
| `assetName` | string | yes | Request body value for AssetName. |
| `assetDescription` | string | yes | Request body value for AssetDescription. |
| `assetDate` | date | yes | Request body value for AssetDate. |
| `ownerAsset` | string | yes | Request body value for OwnerAsset. |
| `purchaseOrderNo` | string | yes | Request body value for PurchaseOrderNo. |
| `purchaseOrderLineNo` | string | yes | Request body value for PurchaseOrderLineNo. |
| `note` | string | yes | Request body value for Note. |
| `group1` | string | yes | Request body value for Group1. |
| `group2` | string | yes | Request body value for Group2. |
| `group3` | string | yes | Request body value for Group3. |
| `group4` | string | yes | Request body value for Group4. |
| `group5` | string | yes | Request body value for Group5. |
| `group6` | string | yes | Request body value for Group6. |
| `invoiceAccountCodingLineNo` | number | yes | Request body value for InvoiceAccountCodingLineNo. |
| `allocationType` | string | yes | Request body value for AllocationType. |
| `lineVatAmount` | number | yes | Request body value for LineVatAmount. |
| `vatCalculationRule` | string | yes | Request body value for VatCalculationRule. |
| `purchaseOrderLineId` | number | yes | Request body value for PurchaseOrderLineId. |
| `queueType` | number | yes | Request body value for QueueType. |
| `queueStatus` | number | yes | Request body value for QueueStatus. |
| `errorText` | string | yes | Request body value for ErrorText. |
| `invoiceAccountCodingId` | number | yes | Request body value for InvoiceAccountCodingId. |
| `rowIndex` | number | yes | Request body value for RowIndex. |
| `invoiceQueueId` | number | yes | Request body value for InvoiceQueueId. |
| `type` | string | yes | Request body value for Type. |
| `createUser` | string | yes | Request body value for CreateUser. |
| `createRole` | string | yes | Request body value for CreateRole. |
| `signUser` | string | yes | Request body value for SignUser. |
| `signRole` | string | yes | Request body value for SignRole. |
| `acceptUser` | string | yes | Request body value for AcceptUser. |
| `acceptRole` | string | yes | Request body value for AcceptRole. |
| `account` | string | yes | Request body value for Account. |
| `object1` | string | yes | Request body value for Object1. |
| `object2` | string | yes | Request body value for Object2. |
| `object3` | string | yes | Request body value for Object3. |
| `object4` | string | yes | Request body value for Object4. |
| `object5` | string | yes | Request body value for Object5. |
| `object6` | string | yes | Request body value for Object6. |
| `object7` | string | yes | Request body value for Object7. |
| `object8` | string | yes | Request body value for Object8. |
| `currency` | string | yes | Request body value for Currency. |
| `amount` | number | yes | Request body value for Amount. |
| `baseAmount` | number | yes | Request body value for BaseAmount. |
| `number` | number | yes | Request body value for Number. |
| `vatCode` | string | yes | Request body value for VatCode. |
| `vatDeduction` | number | yes | Request body value for VatDeduction. |
| `allocationsAccount` | string | yes | Request body value for AllocationsAccount. |
| `allocateFromDate` | date | yes | Request body value for AllocateFromDate. |
| `allocateToDate` | date | yes | Request body value for AllocateToDate. |
| `forwardInvoice` | string | yes | Request body value for ForwardInvoice. |
| `assetType` | string | yes | Request body value for AssetType. |
| `assetName` | string | yes | Request body value for AssetName. |
| `assetDescription` | string | yes | Request body value for AssetDescription. |
| `assetDate` | date | yes | Request body value for AssetDate. |
| `ownerAsset` | string | yes | Request body value for OwnerAsset. |
| `purchaseOrderNo` | string | yes | Request body value for PurchaseOrderNo. |
| `purchaseOrderLineNo` | string | yes | Request body value for PurchaseOrderLineNo. |
| `note` | string | yes | Request body value for Note. |
| `group1` | string | yes | Request body value for Group1. |
| `group2` | string | yes | Request body value for Group2. |
| `group3` | string | yes | Request body value for Group3. |
| `group4` | string | yes | Request body value for Group4. |
| `group5` | string | yes | Request body value for Group5. |
| `group6` | string | yes | Request body value for Group6. |
| `invoiceAccountCodingLineNo` | number | yes | Request body value for InvoiceAccountCodingLineNo. |
| `allocationType` | string | yes | Request body value for AllocationType. |
| `lineVatAmount` | number | yes | Request body value for LineVatAmount. |
| `vatCalculationRule` | string | yes | Request body value for VatCalculationRule. |
| `purchaseOrderLineId` | number | yes | Request body value for PurchaseOrderLineId. |
| `queueType` | number | yes | Request body value for QueueType. |
| `queueStatus` | number | yes | Request body value for QueueStatus. |
| `errorText` | string | yes | Request body value for ErrorText. |
| `invoiceAccountCodingId` | number | yes | Request body value for InvoiceAccountCodingId. |
| `rowIndex` | number | yes | Request body value for RowIndex. |
| `invoiceQueueId` | number | yes | Request body value for InvoiceQueueId. |
| `type` | string | yes | Request body value for Type. |
| `createUser` | string | yes | Request body value for CreateUser. |
| `createRole` | string | yes | Request body value for CreateRole. |
| `signUser` | string | yes | Request body value for SignUser. |
| `signRole` | string | yes | Request body value for SignRole. |
| `acceptUser` | string | yes | Request body value for AcceptUser. |
| `acceptRole` | string | yes | Request body value for AcceptRole. |
| `account` | string | yes | Request body value for Account. |
| `object1` | string | yes | Request body value for Object1. |
| `object2` | string | yes | Request body value for Object2. |
| `object3` | string | yes | Request body value for Object3. |
| `object4` | string | yes | Request body value for Object4. |
| `object5` | string | yes | Request body value for Object5. |
| `object6` | string | yes | Request body value for Object6. |
| `object7` | string | yes | Request body value for Object7. |
| `object8` | string | yes | Request body value for Object8. |
| `currency` | string | yes | Request body value for Currency. |
| `amount` | number | yes | Request body value for Amount. |
| `baseAmount` | number | yes | Request body value for BaseAmount. |
| `number` | number | yes | Request body value for Number. |
| `vatCode` | string | yes | Request body value for VatCode. |
| `vatDeduction` | number | yes | Request body value for VatDeduction. |
| `allocationsAccount` | string | yes | Request body value for AllocationsAccount. |
| `allocateFromDate` | date | yes | Request body value for AllocateFromDate. |
| `allocateToDate` | date | yes | Request body value for AllocateToDate. |
| `forwardInvoice` | string | yes | Request body value for ForwardInvoice. |
| `assetType` | string | yes | Request body value for AssetType. |
| `assetName` | string | yes | Request body value for AssetName. |
| `assetDescription` | string | yes | Request body value for AssetDescription. |
| `assetDate` | date | yes | Request body value for AssetDate. |
| `ownerAsset` | string | yes | Request body value for OwnerAsset. |
| `purchaseOrderNo` | string | yes | Request body value for PurchaseOrderNo. |
| `purchaseOrderLineNo` | string | yes | Request body value for PurchaseOrderLineNo. |
| `note` | string | yes | Request body value for Note. |
| `group1` | string | yes | Request body value for Group1. |
| `group2` | string | yes | Request body value for Group2. |
| `group3` | string | yes | Request body value for Group3. |
| `group4` | string | yes | Request body value for Group4. |
| `group5` | string | yes | Request body value for Group5. |
| `group6` | string | yes | Request body value for Group6. |
| `invoiceAccountCodingLineNo` | number | yes | Request body value for InvoiceAccountCodingLineNo. |
| `allocationType` | string | yes | Request body value for AllocationType. |
| `lineVatAmount` | number | yes | Request body value for LineVatAmount. |
| `vatCalculationRule` | string | yes | Request body value for VatCalculationRule. |
| `purchaseOrderLineId` | number | yes | Request body value for PurchaseOrderLineId. |
| `queueType` | number | yes | Request body value for QueueType. |
| `queueStatus` | number | yes | Request body value for QueueStatus. |
| `errorText` | string | yes | Request body value for ErrorText. |
| `invoiceAccountCodingId` | number | yes | Request body value for InvoiceAccountCodingId. |
| `rowIndex` | number | yes | Request body value for RowIndex. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Rillion Prime API returns.

## Native endpoint

Through the native Rillion Prime API, this operation is `PUT /invoiceaccountcodingqueue/:invoiceaccountcodingqueueid` (base URL `{{credentials.baseUrl}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-invoice-account-coding-queue.md) for the provider-specific parameters and requirements.

