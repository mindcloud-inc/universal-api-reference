# Create Invoice Diary Post with Rillion Prime

## Endpoint

- **Method:** `POST`
- **Path:** `/invoice/diary`
- **Base URL:** `{baseUrl}`
- **Official documentation:** [Create Invoice Diary Post](https://prime-2-uat-14-ue.rillionprime.com/swagger/index.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `invoiceDiary` | body | `object` | yes | Request body value for InvoiceDiary. |
| `invoiceDiary.headersOnly` | body | `number` | yes | Request body value for InvoiceDiary HeadersOnly. |
| `invoiceDiary.forProcessing` | body | `boolean` | yes | Request body value for InvoiceDiary ForProcessing. |
| `invoiceDiary.locked` | body | `boolean` | yes | Request body value for InvoiceDiary Locked. |
| `invoiceDiary.lockedRowId` | body | `number` | yes | Request body value for InvoiceDiary LockedRowId. |
| `invoiceDiary.lockedRowLoginName` | body | `string` | yes | Request body value for InvoiceDiary LockedRowLoginName. |
| `invoiceDiary.lockedRowRole` | body | `string` | yes | Request body value for InvoiceDiary LockedRowRole. |
| `invoiceDiary.rowState` | body | `number` | yes | Request body value for InvoiceDiary RowState. |
| `invoiceDiary.selected` | body | `boolean` | yes | Request body value for InvoiceDiary Selected. |
| `invoiceDiary.keyValuesRowState` | body | `number` | yes | Request body value for InvoiceDiary KeyValuesRowState. |
| `invoiceDiary.invoiceDiaryId` | body | `number` | yes | Request body value for InvoiceDiary InvoiceDiaryId. |
| `invoiceDiary.invoiceId` | body | `number` | yes | Request body value for InvoiceDiary InvoiceId. |
| `invoiceDiary.type` | body | `number` | yes | Request body value for InvoiceDiary Type. |
| `invoiceDiary.investigateType` | body | `number` | yes | Request body value for InvoiceDiary InvestigateType. |
| `invoiceDiary.createTime` | body | `date` | yes | Request body value for InvoiceDiary CreateTime. |
| `invoiceDiary.createUser` | body | `string` | yes | Request body value for InvoiceDiary CreateUser. |
| `invoiceDiary.createRole` | body | `string` | yes | Request body value for InvoiceDiary CreateRole. |
| `invoiceDiary.investigateRole` | body | `string` | yes | Request body value for InvoiceDiary InvestigateRole. |
| `invoiceDiary.note` | body | `string` | yes | Request body value for InvoiceDiary Note. |
| `invoiceDiary.attachedFile` | body | `string` | yes | Request body value for InvoiceDiary AttachedFile. |
| `invoiceDiary.visibleInSupplierPortal` | body | `boolean` | yes | Request body value for InvoiceDiary VisibleInSupplierPortal. |
| `invoiceDiary.createUserFullName` | body | `string` | yes | Request body value for InvoiceDiary CreateUserFullName. |
| `invoiceDiary` | body | `object` | yes | Request body value for InvoiceDiary. |
| `invoiceDiary.headersOnly` | body | `number` | yes | Request body value for InvoiceDiary HeadersOnly. |
| `invoiceDiary.forProcessing` | body | `boolean` | yes | Request body value for InvoiceDiary ForProcessing. |
| `invoiceDiary.locked` | body | `boolean` | yes | Request body value for InvoiceDiary Locked. |
| `invoiceDiary.lockedRowId` | body | `number` | yes | Request body value for InvoiceDiary LockedRowId. |
| `invoiceDiary.lockedRowLoginName` | body | `string` | yes | Request body value for InvoiceDiary LockedRowLoginName. |
| `invoiceDiary.lockedRowRole` | body | `string` | yes | Request body value for InvoiceDiary LockedRowRole. |
| `invoiceDiary.rowState` | body | `number` | yes | Request body value for InvoiceDiary RowState. |
| `invoiceDiary.selected` | body | `boolean` | yes | Request body value for InvoiceDiary Selected. |
| `invoiceDiary.keyValuesRowState` | body | `number` | yes | Request body value for InvoiceDiary KeyValuesRowState. |
| `invoiceDiary.invoiceDiaryId` | body | `number` | yes | Request body value for InvoiceDiary InvoiceDiaryId. |
| `invoiceDiary.invoiceId` | body | `number` | yes | Request body value for InvoiceDiary InvoiceId. |
| `invoiceDiary.type` | body | `number` | yes | Request body value for InvoiceDiary Type. |
| `invoiceDiary.investigateType` | body | `number` | yes | Request body value for InvoiceDiary InvestigateType. |
| `invoiceDiary.createTime` | body | `date` | yes | Request body value for InvoiceDiary CreateTime. |
| `invoiceDiary.createUser` | body | `string` | yes | Request body value for InvoiceDiary CreateUser. |
| `invoiceDiary.createRole` | body | `string` | yes | Request body value for InvoiceDiary CreateRole. |
| `invoiceDiary.investigateRole` | body | `string` | yes | Request body value for InvoiceDiary InvestigateRole. |
| `invoiceDiary.note` | body | `string` | yes | Request body value for InvoiceDiary Note. |
| `invoiceDiary.attachedFile` | body | `string` | yes | Request body value for InvoiceDiary AttachedFile. |
| `invoiceDiary.visibleInSupplierPortal` | body | `boolean` | yes | Request body value for InvoiceDiary VisibleInSupplierPortal. |
| `invoiceDiary.createUserFullName` | body | `string` | yes | Request body value for InvoiceDiary CreateUserFullName. |
| `invoiceDiary` | body | `object` | yes | Request body value for InvoiceDiary. |
| `invoiceDiary.headersOnly` | body | `number` | yes | Request body value for InvoiceDiary HeadersOnly. |
| `invoiceDiary.forProcessing` | body | `boolean` | yes | Request body value for InvoiceDiary ForProcessing. |
| `invoiceDiary.locked` | body | `boolean` | yes | Request body value for InvoiceDiary Locked. |
| `invoiceDiary.lockedRowId` | body | `number` | yes | Request body value for InvoiceDiary LockedRowId. |
| `invoiceDiary.lockedRowLoginName` | body | `string` | yes | Request body value for InvoiceDiary LockedRowLoginName. |
| `invoiceDiary.lockedRowRole` | body | `string` | yes | Request body value for InvoiceDiary LockedRowRole. |
| `invoiceDiary.rowState` | body | `number` | yes | Request body value for InvoiceDiary RowState. |
| `invoiceDiary.selected` | body | `boolean` | yes | Request body value for InvoiceDiary Selected. |
| `invoiceDiary.keyValuesRowState` | body | `number` | yes | Request body value for InvoiceDiary KeyValuesRowState. |
| `invoiceDiary.invoiceDiaryId` | body | `number` | yes | Request body value for InvoiceDiary InvoiceDiaryId. |
| `invoiceDiary.invoiceId` | body | `number` | yes | Request body value for InvoiceDiary InvoiceId. |
| `invoiceDiary.type` | body | `number` | yes | Request body value for InvoiceDiary Type. |
| `invoiceDiary.investigateType` | body | `number` | yes | Request body value for InvoiceDiary InvestigateType. |
| `invoiceDiary.createTime` | body | `date` | yes | Request body value for InvoiceDiary CreateTime. |
| `invoiceDiary.createUser` | body | `string` | yes | Request body value for InvoiceDiary CreateUser. |
| `invoiceDiary.createRole` | body | `string` | yes | Request body value for InvoiceDiary CreateRole. |
| `invoiceDiary.investigateRole` | body | `string` | yes | Request body value for InvoiceDiary InvestigateRole. |
| `invoiceDiary.note` | body | `string` | yes | Request body value for InvoiceDiary Note. |
| `invoiceDiary.attachedFile` | body | `string` | yes | Request body value for InvoiceDiary AttachedFile. |
| `invoiceDiary.visibleInSupplierPortal` | body | `boolean` | yes | Request body value for InvoiceDiary VisibleInSupplierPortal. |
| `invoiceDiary.createUserFullName` | body | `string` | yes | Request body value for InvoiceDiary CreateUserFullName. |
