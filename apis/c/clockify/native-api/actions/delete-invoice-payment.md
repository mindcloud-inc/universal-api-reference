# Delete Invoice Payment with Clockify

Deletes an existing invoice payment from Clockify.

## Endpoint

- **Method:** `DELETE`
- **Path:** `workspaces/:workspaceId/invoices/:invoiceId/payments/:paymentId`
- **Base URL:** `https://api.clockify.me/api/v1`
- **Official documentation:** [Delete Invoice Payment](https://docs.developer.clockify.me/#tag/Invoice/operation/deletePaymentById)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `workspaceId` | path | `list<string>` | yes |
| `invoiceId` | path | `string<string>` | yes |
| `paymentId` | path | `string<string>` | yes |
