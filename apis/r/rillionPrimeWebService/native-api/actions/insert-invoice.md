# Insert Invoice with Rillion Prime Web Service

Insert an invoice into the Prime invoice queue.

## Endpoint

- **Method:** `POST`
- **Base URL:** `{baseUrl}`

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `Invoice` | body | `object` | yes | Fill in the fields below, or use Use Variables ({}) on this object to map the whole payload from a previous step. Field semantics: Prime Integration Tables, Invoice section. |
| `Invoice.InvoiceSeries` | body | `string` | yes | Invoice series |
| `Invoice.InvoiceNo` | body | `number` | yes | Invoice number |
| `Invoice.Company` | body | `list<string>` | yes | Company |
| `Invoice.Credit` | body | `string` | yes | Credit note: 0=No; 1=Yes |
| `Invoice.Type` | body | `number` | yes | Invoice type: 0=External; 1=Internal; 2=Expense |
| `Invoice.Status` | body | `number` | yes | Invoice status: 0=Being processed/for preliminary recording; 2=Ready for deletion; 4=Ready for definite recording; 5=Update account coding on import; 6=Updated account coding on active invoice |
| `Invoice.Classified` | body | `string` | yes | Classified invoice: 0=No; 1=Yes |
| `Invoice.Blocked` | body | `string` | yes | Blocked for payment: 0=No; 1=Yes |
| `Invoice.Supplier` | body | `string` | yes | Supplier ID |
| `Invoice.SupplierInvoiceNo` | body | `string` | yes | Supplier’s invoice number |
| `Invoice.PurchaseOrderNo` | body | `string` | no | Order number |
| `Invoice.ContractNo` | body | `string` | no | Contract number |
| `Invoice.InvoiceDate` | body | `date` | yes | Invoice date |
| `Invoice.DueDate` | body | `date` | yes | Due date |
| `Invoice.AccountCodingDate` | body | `date` | yes | Accounting date |
| `Invoice.Currency` | body | `string` | yes | Currency on posting line |
| `Invoice.Amount` | body | `number` | yes | — |
| `Invoice.BaseAmount` | body | `number` | yes | Amount in currency for accounting purposes |
| `Invoice.VatAmount` | body | `number` | yes | VAT amount in the invoice’s currency |
| `Invoice.BaseVatAmount` | body | `number` | yes | VAT amount in currency for accounting purposes |
| `Invoice.FeeAmount1` | body | `number` | yes | Extra fee type 1 |
| `Invoice.FeeAmount2` | body | `number` | yes | Extra fee type 2 |
| `Invoice.FeeAmount3` | body | `number` | yes | Extra fee type 3 |
| `Invoice.PaymentAmount` | body | `number` | yes | Amount payable when QueueType=2 |
| `Invoice.AuthorizationUser` | body | `string` | no | Signed by user |
| `Invoice.AuthorizationRole` | body | `string` | no | Signed by role |
| `Invoice.DebtAccount` | body | `string` | yes | Trade creditors account |
| `Invoice.Account` | body | `string` | yes | Account |
| `Invoice.Object1` | body | `string` | no | Object of Type 1 |
| `Invoice.Object2` | body | `string` | no | Object of Type 2 |
| `Invoice.Object3` | body | `string` | no | Object of Type 3 |
| `Invoice.Object4` | body | `string` | no | Object of Type 4 |
| `Invoice.Object5` | body | `string` | no | Object of Type 5 |
| `Invoice.Object6` | body | `string` | no | Object of Type 6 |
| `Invoice.Object7` | body | `string` | no | Object of Type 7 |
| `Invoice.Object8` | body | `string` | no | Object of Type 8 |
| `Invoice.VatCode` | body | `string` | yes | VAT code |
| `Invoice.ArrivalAccountCoded` | body | `string` | yes | Preliminary recorded: 0=No; 1=Yes |
| `Invoice.ArrivalAccountCodingDate` | body | `date` | no | Preliminary recording date |
| `Invoice.Asset` | body | `string` | yes | Refers to an asset record: 0=No; 1=Yes |
| `Invoice.VoucherSeries` | body | `string` | no | Voucher series |
| `Invoice.VoucherNo` | body | `number` | no | Voucher number |
| `Invoice.PaymentDate` | body | `date` | no | Date for final payment of the invoice |
| `Invoice.AlternativeID` | body | `string` | no | Alternative ID |
| `Invoice.LinkedInvoiceSeries` | body | `string` | no | Invoice series of invoice that invoice is linked to, e.g. credit note |
| `Invoice.LinkedInvoiceNo` | body | `number` | no | Invoice number of invoice that invoice is linked to, e.g. credit note |
| `Invoice.PayReference` | body | `string` | no | Payment reference number, e.g. OCR/IBAN/KID |
| `Invoice.DeliveryNote` | body | `string` | no | GRN refering to the invoice |
| `Invoice.ExtraID` | body | `string` | no | Extra identification field |
| `Invoice.ExtraAmount` | body | `number` | no | Extra amount field |
| `Invoice.PurchaseOrderMatch` | body | `number` | yes | See Appendix A for match status. |
| `Invoice.PurchaseOrderMatchType` | body | `number` | no | — |
| `Invoice.Reference1` | body | `string` | no | Invoice reference 1 |
| `Invoice.Reference2` | body | `string` | no | Invoice reference 2 |
| `Invoice.Note` | body | `string` | no | Free text |
| `Invoice.Group1` | body | `string` | no | Free group 1 |
| `Invoice.Group2` | body | `string` | no | Free group 2 |
| `Invoice.Group3` | body | `string` | no | Free group 3 |
| `Invoice.Group4` | body | `string` | no | Free group 4 |
| `Invoice.Group5` | body | `string` | no | Free group 5 |
| `Invoice.Group6` | body | `string` | no | Free group 6 |
| `Invoice.PaymentMessage` | body | `string` | no | Payment message |
| `Invoice.AccountCoding[]` | body | `array<object>` | no | Account Coding lines. |
| `Invoice.AccountCoding[].Type` | body | `number` | yes | Type of posting line: 0=Trade creds; 1=Expenses line; 2=VAT line |
| `Invoice.AccountCoding[].CreateUser` | body | `string` | no | Created by user |
| `Invoice.AccountCoding[].CreateRole` | body | `string` | no | Created by role |
| `Invoice.AccountCoding[].AcceptUser` | body | `string` | no | Acceptance user from external ERP |
| `Invoice.AccountCoding[].AcceptRole` | body | `string` | no | Acceptance role from external ERP |
| `Invoice.AccountCoding[].SignUser` | body | `string` | no | Signed by user |
| `Invoice.AccountCoding[].SignRole` | body | `string` | no | Signed by role |
| `Invoice.AccountCoding[].Account` | body | `string` | yes | Account |
| `Invoice.AccountCoding[].Object1` | body | `string` | no | Object of Type 1 |
| `Invoice.AccountCoding[].Object2` | body | `string` | no | Object of Type 2 |
| `Invoice.AccountCoding[].Object3` | body | `string` | no | Object of Type 3 |
| `Invoice.AccountCoding[].Object4` | body | `string` | no | Object of Type 4 |
| `Invoice.AccountCoding[].Object5` | body | `string` | no | Object of Type 5 |
| `Invoice.AccountCoding[].Object6` | body | `string` | no | Object of Type 6 |
| `Invoice.AccountCoding[].Object7` | body | `string` | no | Object of Type 7 |
| `Invoice.AccountCoding[].Object8` | body | `string` | no | Object of Type 8 |
| `Invoice.AccountCoding[].Currency` | body | `string` | yes | Currency on posting line |
| `Invoice.AccountCoding[].Amount` | body | `number` | yes | — |
| `Invoice.AccountCoding[].BaseAmount` | body | `number` | yes | Amount in currency for accounting purposes |
| `Invoice.AccountCoding[].InvoiceAccountCodingLineNo` | body | `number` | no | Line number |
| `Invoice.AccountCoding[].LineVatAmount` | body | `number` | yes | Calculated line VAT amount |
| `Invoice.AccountCoding[].Number` | body | `number` | no | Quantity |
| `Invoice.AccountCoding[].VatCode` | body | `string` | yes | VAT code |
| `Invoice.AccountCoding[].VatDeduction` | body | `number` | yes | — |
| `Invoice.AccountCoding[].AllocationType` | body | `string` | no | Allocation type |
| `Invoice.AccountCoding[].AllocationsAccount` | body | `string` | no | Allocations account |
| `Invoice.AccountCoding[].AllocateFromDate` | body | `date` | no | Allocate from |
| `Invoice.AccountCoding[].AllocateToDate` | body | `date` | no | Allocate until |
| `Invoice.AccountCoding[].ForwardInvoice` | body | `number` | yes | Reinvoice: 0=No; 1=For reinvoicing; 2=Reinvoiced |
| `Invoice.AccountCoding[].AssetType` | body | `string` | no | Asset type |
| `Invoice.AccountCoding[].AssetName` | body | `string` | no | Asset name |
| `Invoice.AccountCoding[].AssetDescription` | body | `string` | no | Asset description |
| `Invoice.AccountCoding[].AssetDate` | body | `date` | no | Purchase date for asset |
| `Invoice.AccountCoding[].OwnerAsset` | body | `string` | no | Belongs to existing asset |
| `Invoice.AccountCoding[].PurchaseOrderNo` | body | `string` | no | Order number |
| `Invoice.AccountCoding[].PurchaseOrderLineNo` | body | `string` | no | Order line ID |
| `Invoice.AccountCoding[].Note` | body | `string` | no | Free text |
| `Invoice.AccountCoding[].Group1` | body | `string` | no | Free group 1 |
| `Invoice.AccountCoding[].Group2` | body | `string` | no | Free group 2 |
| `Invoice.AccountCoding[].Group3` | body | `string` | no | Free group 3 |
| `Invoice.AccountCoding[].Group4` | body | `string` | no | Free group 4 |
| `Invoice.AccountCoding[].Group5` | body | `string` | no | Free group 5 |
| `Invoice.AccountCoding[].Group6` | body | `string` | no | Free group 6 |
| `Invoice.AccountCoding[].PurchaseOrderItem` | body | `string` | no | — |
| `Invoice.AccountCoding[].CurrencyExternalId` | body | `string` | no | — |
| `Invoice.AccountCoding[].CurrencyExternalSource` | body | `string` | no | — |
| `Invoice.AccountCoding[].PurchaseOrderExternalId` | body | `string` | no | — |
| `Invoice.AccountCoding[].PurchaseOrderExternalSource` | body | `string` | no | — |
| `Invoice.AccountCoding[].VatCodeExternalId` | body | `string` | no | — |
| `Invoice.AccountCoding[].VatCodeExternalSource` | body | `string` | no | — |
| `Invoice.AccountCoding[].AccountExternalId` | body | `string` | no | — |
| `Invoice.AccountCoding[].AccountExternalSource` | body | `string` | no | — |
| `Invoice.AccountCoding[].AssetExternalId` | body | `string` | no | — |
| `Invoice.AccountCoding[].AssetExternalSource` | body | `string` | no | — |
| `Invoice.AccountCoding[].Object1ExternalId` | body | `string` | no | — |
| `Invoice.AccountCoding[].Object1ExternalSource` | body | `string` | no | — |
| `Invoice.AccountCoding[].Object2ExternalId` | body | `string` | no | — |
| `Invoice.AccountCoding[].Object2ExternalSource` | body | `string` | no | — |
| `Invoice.AccountCoding[].Object3ExternalId` | body | `string` | no | — |
| `Invoice.AccountCoding[].Object3ExternalSource` | body | `string` | no | — |
| `Invoice.AccountCoding[].Object4ExternalId` | body | `string` | no | — |
| `Invoice.AccountCoding[].Object4ExternalSource` | body | `string` | no | — |
| `Invoice.AccountCoding[].Object5ExternalId` | body | `string` | no | — |
| `Invoice.AccountCoding[].Object5ExternalSource` | body | `string` | no | — |
| `Invoice.AccountCoding[].Object6ExternalId` | body | `string` | no | — |
| `Invoice.AccountCoding[].Object6ExternalSource` | body | `string` | no | — |
| `Invoice.AccountCoding[].Object7ExternalId` | body | `string` | no | — |
| `Invoice.AccountCoding[].Object7ExternalSource` | body | `string` | no | — |
| `Invoice.AccountCoding[].Object8ExternalId` | body | `string` | no | — |
| `Invoice.AccountCoding[].Object8ExternalSource` | body | `string` | no | — |
| `Invoice.ContractMatch` | body | `number` | yes | Invoice matched to a Contract: 0=Not matched to a Contract; 1=Partly matched to a Contract; 2=Fully matched to a Contract |
| `Invoice.SupplierBankAccount` | body | `string` | no | Bankaccount for payment |
| `Invoice.UseDiscount` | body | `boolean` | yes | Make use or the cash discount: 0=No; 1=Yes |
| `Invoice.DiscountGrossAmount` | body | `boolean` | yes | DiscountAmount calculation based on Gross Amount 0=No; 1=Yes |
| `Invoice.DiscountDate` | body | `date` | no | Payment date to make use of the cash discount |
| `Invoice.DiscountAmount` | body | `number` | no | Payment amount if make use of the cash discount |
| `Invoice.DiscountPercentage` | body | `number` | yes | Discount percentage used in calculation of DiscountAmount |
| `Invoice.ExternalId` | body | `string` | no | — |
| `Invoice.ExternalSource` | body | `string` | no | — |
| `Invoice.LinkedInvoiceExternalId` | body | `string` | no | — |
| `Invoice.LinkedInvoiceExternalSource` | body | `string` | no | — |
| `Invoice.SupplierExternalId` | body | `string` | no | — |
| `Invoice.SupplierExternalSource` | body | `string` | no | — |
| `Invoice.PurchaseOrderExternalId` | body | `string` | no | — |
| `Invoice.PurchaseOrderExternalSource` | body | `string` | no | — |
| `Invoice.VatCodeExternalId` | body | `string` | no | — |
| `Invoice.VatCodeExternalSource` | body | `string` | no | — |
| `Invoice.CurrencyExternalId` | body | `string` | no | — |
| `Invoice.CurrencyExternalSource` | body | `string` | no | — |
| `Invoice.AccountExternalId` | body | `string` | no | — |
| `Invoice.AccountExternalSource` | body | `string` | no | — |
| `Invoice.SupplierBankAccountExternalId` | body | `string` | no | — |
| `Invoice.SupplierBankAccountExternalSource` | body | `string` | no | — |
| `Invoice.Object1ExternalId` | body | `string` | no | — |
| `Invoice.Object1ExternalSource` | body | `string` | no | — |
| `Invoice.ObjectType1ExternalId` | body | `string` | no | — |
| `Invoice.ObjectType1ExternalSource` | body | `string` | no | — |
| `Invoice.Object2ExternalId` | body | `string` | no | — |
| `Invoice.Object2ExternalSource` | body | `string` | no | — |
| `Invoice.ObjectType2ExternalId` | body | `string` | no | — |
| `Invoice.ObjectType2ExternalSource` | body | `string` | no | — |
| `Invoice.Object3ExternalId` | body | `string` | no | — |
| `Invoice.Object3ExternalSource` | body | `string` | no | — |
| `Invoice.ObjectType3ExternalId` | body | `string` | no | — |
| `Invoice.ObjectType3ExternalSource` | body | `string` | no | — |
| `Invoice.Object4ExternalId` | body | `string` | no | — |
| `Invoice.Object4ExternalSource` | body | `string` | no | — |
| `Invoice.ObjectType4ExternalId` | body | `string` | no | — |
| `Invoice.ObjectType4ExternalSource` | body | `string` | no | — |
| `Invoice.Object5ExternalId` | body | `string` | no | — |
| `Invoice.Object5ExternalSource` | body | `string` | no | — |
| `Invoice.ObjectType5ExternalId` | body | `string` | no | — |
| `Invoice.ObjectType5ExternalSource` | body | `string` | no | — |
| `Invoice.Object6ExternalId` | body | `string` | no | — |
| `Invoice.Object6ExternalSource` | body | `string` | no | — |
| `Invoice.ObjectType6ExternalId` | body | `string` | no | — |
| `Invoice.ObjectType6ExternalSource` | body | `string` | no | — |
| `Invoice.Object7ExternalId` | body | `string` | no | — |
| `Invoice.Object7ExternalSource` | body | `string` | no | — |
| `Invoice.ObjectType7ExternalId` | body | `string` | no | — |
| `Invoice.ObjectType7ExternalSource` | body | `string` | no | — |
| `Invoice.Object8ExternalId` | body | `string` | no | — |
| `Invoice.Object8ExternalSource` | body | `string` | no | — |
| `Invoice.ObjectType8ExternalId` | body | `string` | no | — |
| `Invoice.ObjectType8ExternalSource` | body | `string` | no | — |
| `TransferFromQueue` | body | `boolean` | yes | Process the record from the queue immediately. Leave true unless your Rillion contact advises otherwise. |
