# Insert Supplier with Rillion Prime Web Service

Insert a supplier into the Prime register queue.

## Endpoint

- **Method:** `POST`
- **Base URL:** `{baseUrl}`

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `Supplier` | body | `object` | yes | Fill in the fields below, or use Use Variables ({}) on this object to map the whole payload from a previous step. Field semantics: Prime Integration Tables, Supplier section. |
| `Supplier.Company` | body | `list<string>` | no | Company |
| `Supplier.Supplier` | body | `string` | yes | Supplier number in ERP system |
| `Supplier.Name` | body | `string` | no | Name of the Bank or other description |
| `Supplier.Type` | body | `number` | no | Supplier type: 0=External; 1=Internal; 2=Temporary |
| `Supplier.VatNo` | body | `string` | no | VAT registration number |
| `Supplier.Ean` | body | `string` | no | EAN code |
| `Supplier.Iban` | body | `string` | no | IBAN |
| `Supplier.GraceDays` | body | `string` | no | Grace days before payment, this value is translated to a payment term in Palette |
| `Supplier.PaymentTerm` | body | `string` | no | Payment term. The Payment term can also be set by using GraceDays |
| `Supplier.Blocked` | body | `number` | no | Block invoices from the supplier: 0=No; 1=Invoices cannot be transferred from invoice log; 2=Blocked for payment |
| `Supplier.Classified` | body | `number` | no | Classify: 0=No; 1=Yes |
| `Supplier.IsPerson` | body | `number` | no | Is person: 0=No; 1=Yes |
| `Supplier.ValidTo` | body | `date` | no | A valid to date for a supplier |
| `Supplier.CashDiscount` | body | `number` | no | Apply the supplier cash discount: 0=No; 1=Yes |
| `Supplier.Currency` | body | `string` | no | Default currency for supplier |
| `Supplier.DebtAccount` | body | `string` | no | Trade creditors account |
| `Supplier.CostAccount` | body | `string` | no | Default expenditure account |
| `Supplier.VatCode` | body | `string` | no | VAT codes |
| `Supplier.VatType` | body | `string` | no | VatType |
| `Supplier.FlowProposal` | body | `string` | no | Default flowproposal for the supplier |
| `Supplier.Object1` | body | `string` | no | Object of Type 1 linked to the supplier |
| `Supplier.Object2` | body | `string` | no | Object of Type 2 linked to the supplier |
| `Supplier.Object3` | body | `string` | no | Object of Type 3 linked to the supplier |
| `Supplier.Object4` | body | `string` | no | Object of Type 4 linked to the supplier |
| `Supplier.Object5` | body | `string` | no | Object of Type 5 linked to the supplier |
| `Supplier.Object6` | body | `string` | no | Object of Type 6 linked to the supplier |
| `Supplier.Object7` | body | `string` | no | Object of Type 7 linked to the supplier |
| `Supplier.Object8` | body | `string` | no | Object of Type 8 linked to the supplier |
| `Supplier.Address1` | body | `string` | no | Address detail 1 |
| `Supplier.Address2` | body | `string` | no | Address detail 2 |
| `Supplier.Address3` | body | `string` | no | Address detail 3 |
| `Supplier.Address4` | body | `string` | no | Address detail 4 |
| `Supplier.Address5` | body | `string` | no | Address detail 5 |
| `Supplier.Address6` | body | `string` | no | Address detail 6 |
| `Supplier.Tele1` | body | `string` | no | Telephone detail 1 |
| `Supplier.Tele2` | body | `string` | no | Telephone detail 2 |
| `Supplier.Tele3` | body | `string` | no | Telephone detail 3 |
| `Supplier.Www` | body | `string` | no | Internet address |
| `Supplier.Contact` | body | `string` | no | Contact person |
| `Supplier.Email` | body | `string` | no | E-mail to contact person |
| `Supplier.PurchaseOrderEmail` | body | `string` | no | E-mail to contact person for purchaseorder |
| `Supplier.CorporateIdentityNo` | body | `string` | no | Corporate Identity Number |
| `Supplier.Note` | body | `string` | no | Notes on supplier |
| `Supplier.LanguageID` | body | `string` | no | Preferred language |
| `Supplier.Group1` | body | `string` | no | Free group 1 |
| `Supplier.Group2` | body | `string` | no | Free group 2 |
| `Supplier.Group3` | body | `string` | no | Free group 3 |
| `Supplier.Remove` | body | `number` | no | Should record be removed: 0=No; 1=Yes |
| `Supplier.KeyType` | body | `number` | no | Is the company included in the primary key for the record: 0=No; 1=Yes |
| `Supplier.CheckPayReference` | body | `number` | no | Check for payment reference: 0=No checking; 1=Rule for global standard; 2=Rule for Finnish standard (GIK); 3=Rule for Swedish standard (OCR); 4=Rule for European standard (RF); 5=Rule for Danish standard (FIK); 6=Rule fo |
| `Supplier.SupplierBankAccount[]` | body | `array<object>` | no | Supplier Bank Account lines. |
| `Supplier.SupplierBankAccount[].BankAccount` | body | `string` | yes | Account number |
| `Supplier.SupplierBankAccount[].Name` | body | `string` | no | Name of the Bank or other description |
| `Supplier.SupplierBankAccount[].Default` | body | `number` | no | Is this Bank Account the default/preferred account number: 0=No; 1=Yes |
| `Supplier.SupplierBankAccount[].ExternalId` | body | `string` | no | — |
| `Supplier.SupplierBankAccount[].ExternalSource` | body | `string` | no | — |
| `Supplier.ExternalId` | body | `string` | no | — |
| `Supplier.ExternalSource` | body | `string` | no | — |
| `TransferFromQueue` | body | `boolean` | yes | Process the record from the queue immediately. Leave true unless your Rillion contact advises otherwise. |
