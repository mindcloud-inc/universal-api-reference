# Update Invoice Settings with Clockify

Updates workspace invoice settings in Clockify.

## Endpoint

- **Method:** `PUT`
- **Path:** `workspaces/:workspaceId/invoices/settings`
- **Base URL:** `https://api.clockify.me/api/v1`
- **Official documentation:** [Update Invoice Settings](https://docs.developer.clockify.me/#tag/Invoice/operation/updateInvoiceSettings)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `workspaceId` | path | `list<string>` | yes |
| `labels` | body | `object` | yes |
| `defaults` | body | `object` | no |
| `exportFields` | body | `object` | no |
| `defaults.companyId` | body | `string` | no |
| `defaults.dueDays` | body | `number` | no |
| `defaults.itemTypeId` | body | `string` | no |
| `defaults.notes` | body | `string` | yes |
| `defaults.subject` | body | `string` | yes |
| `defaults.tax2Percent` | body | `number` | no |
| `defaults.taxPercent` | body | `number` | no |
| `defaults.taxType` | body | `string` | no |
| `exportFields.itemType` | body | `boolean` | no |
| `exportFields.quantity` | body | `boolean` | no |
| `exportFields.rtl` | body | `boolean` | no |
| `exportFields.tax` | body | `boolean` | no |
| `exportFields.tax2` | body | `boolean` | no |
| `exportFields.unitPrice` | body | `boolean` | no |
| `labels.amount` | body | `string` | yes |
| `labels.billFrom` | body | `string` | yes |
| `labels.billTo` | body | `string` | yes |
| `labels.description` | body | `string` | yes |
| `labels.discount` | body | `string` | yes |
| `labels.dueDate` | body | `string` | yes |
| `labels.issueDate` | body | `string` | yes |
| `labels.itemType` | body | `string` | yes |
| `labels.notes` | body | `string` | yes |
| `labels.paid` | body | `string` | yes |
| `labels.quantity` | body | `string` | yes |
| `labels.subtotal` | body | `string` | yes |
| `labels.tax` | body | `string` | yes |
| `labels.tax2` | body | `string` | yes |
| `labels.total` | body | `string` | yes |
| `labels.totalAmountDue` | body | `string` | yes |
| `labels.unitPrice` | body | `string` | yes |
