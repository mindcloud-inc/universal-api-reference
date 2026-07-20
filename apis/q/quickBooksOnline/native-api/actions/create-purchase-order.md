# Create Purchase Order with QuickBooks Online

## Endpoint

- **Method:** `POST`
- **Path:** `/purchaseorder`
- **Base URL:** `https://:quickbooksEnvironment/v3/company/:realmId`
- **Official documentation:** [Create Purchase Order](https://developer.intuit.com/app/developer/qbo/docs/api/accounting/all-entities/purchaseorder#create-a-purchaseorder)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `VendorRef.value` | body | `string` | yes | Vendor Id for the purchase order. |
| `Line[0].Amount` | body | `number` | yes | Amount for the first purchase order expense line. |
| `Line[0].AccountBasedExpenseLineDetail.AccountRef.value` | body | `string` | yes | Expense account ID for the first purchase order line. |
