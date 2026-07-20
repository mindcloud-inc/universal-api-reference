# Send Invoice with QuickBooks Online

## Endpoint

- **Method:** `POST`
- **Path:** `/invoice/:invoiceId/send`
- **Base URL:** `https://:quickbooksEnvironment/v3/company/:realmId`
- **Official documentation:** [Send Invoice](https://developer.intuit.com/app/developer/qbo/docs/api/accounting/all-entities/invoice#send-an-invoice)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `invoiceId` | path | `string` | yes | QuickBooks Invoice Id to send. |
| `sendTo` | query | `string` | no | Optional recipient email for QuickBooks invoice send. If omitted, QuickBooks uses the invoice/customer email on file. |
