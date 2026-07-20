# Update Invoice with Clockify

Updates an existing invoice in Clockify.

## Endpoint

- **Method:** `PUT`
- **Path:** `workspaces/:workspaceId/invoices/:invoiceId`
- **Base URL:** `https://api.clockify.me/api/v1`
- **Official documentation:** [Update Invoice](https://docs.developer.clockify.me/#tag/Invoice/operation/updateInvoice)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `workspaceId` | path | `list<string>` | yes | — |
| `invoiceId` | path | `string<string>` | yes | — |
| `currency` | body | `string` | yes | Maximum length: 100. |
| `discountPercent` | body | `number` | yes | — |
| `dueDate` | body | `date` | yes | — |
| `issuedDate` | body | `date` | yes | — |
| `number` | body | `string` | yes | — |
| `tax2Percent` | body | `number` | yes | — |
| `taxPercent` | body | `number` | yes | — |
| `clientId` | body | `list<string>` | no | — |
| `companyId` | body | `string` | no | — |
| `note` | body | `string` | no | — |
| `subject` | body | `string` | no | — |
| `taxType` | body | `object` | no | — |
| `visibleZeroFields` | body | `list<string>` | no | Accepted values: `DISCOUNT`, `TAX`, `TAX_2`. |
