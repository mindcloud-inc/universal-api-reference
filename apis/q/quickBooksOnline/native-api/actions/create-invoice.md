# Create Invoice with QuickBooks Online

## Endpoint

- **Method:** `POST`
- **Path:** `/invoice`
- **Base URL:** `https://:quickbooksEnvironment/v3/company/:realmId`
- **Official documentation:** [Create Invoice](https://developer.intuit.com/app/developer/qbo/docs/api/accounting/all-entities/invoice#create-an-invoice)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `CustomerRef.value` | body | `string` | yes | Customer Id for the invoice. |
| `Line[0].Amount` | body | `number` | yes | Amount for the first invoice line item. |
| `Line[0].SalesItemLineDetail.ItemRef.value` | body | `string` | yes | Item ID to bill on the first invoice line. |
