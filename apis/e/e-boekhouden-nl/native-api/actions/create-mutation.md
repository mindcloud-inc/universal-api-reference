# Create Mutation with e-Boekhouden.nl

Creates a new mutation in e-Boekhouden.nl.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/mutation`
- **Base URL:** `https://api.e-boekhouden.nl`
- **API:** rest
- **Official documentation:** [Create Mutation](https://api.e-boekhouden.nl/swagger/index.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `type` | body | `string` | yes | A list of mutation types is displayed below. \| Value \| Description \| \|---\|---\| \| 1 \| Invoice received \| \| 2 \| Invoice sent \| \| 3 \| Invoice payment received \| \| 4 \| Invoice payment sent \| \| 5 \| Money received \| \| 6 \| Money sent \| \| 7 \| General journal entry \| |
| `date` | body | `date` | yes | The date of the mutation. Error codes MUT_003 Date is missing. |
| `ledgerId` | body | `number` | yes | The ledger ID of the mutation. Error codes MUTA_001 Ledger id is missing. MUT_007 Unknown ledger for mutation. |
| `invoiceNumber` | body | `string` | no | The invoice number of the mutation. Error codes MUT_018 Invoice number is too long. MUT_019 Invoice number already exists. MUT_002 Invoice number is missing. Maximum length: 50. |
| `entryNumber` | body | `string` | no | The entry of the mutation. Maximum length: 50. |
| `termOfPayment` | body | `number` | no | The term of payment from `date`, in days. Error codes MUT_016 Term of payment is prohibited. |
| `checkPaymentReference` | body | `boolean` | no | If true, the provided `paymentReference` will be validated for uniqueness. |
| `paymentReference` | body | `string` | no | The payment reference of the mutation. |
| `inExVat` | body | `string` | no | Indicates if the amount on mutation rows is including (`IN`) or excluding (`EX`) VAT. The corresponding value will be calculated based on the VAT code. Error codes MUT_017 In/Ex VAT must be 'IN' or 'EX'. MUTA_005 In/Ex VAT is missing. |
| `description` | body | `string` | no | The description of the mutation. Maximum length: 50. |
| `relationId` | body | `number` | no | The relation id of the mutation. Error codes MUT_012 Relation is missing. MUT_013 Relation not found. |
| `rows[].ledgerId` | body | `number` | no | The ledger ID of the row. Required in combination with `type`: 1, 2, 5, 6, 7. For `type` 1, 2, 5, 6 ledger cannot be in the category: `FIN`, `CRED`, `DEB`. For `type` 7 ledger can be any. Error codes MUTA_004 Ledger ID for row is missing. MUT_007 Unknown ledger for mutation. MUT_104 Unknown ledger for row. MUT_106 Invalid ledger category for row. |
| `rows[].vatCode` | body | `string` | yes | A list of VAT codes is displayed below. \| Value \| Description \| \|---\|---\| \| HOOG_VERK_21 \| For selling with 21% VAT. \| \| LAAG_VERK_9 \| For selling with 9% VAT. \| \| VERL_VERK \| For selling with reverse-charging 21% VAT. \| \| VERL_VERK_L9 \| For selling with reverse-charging 9% VAT. \| \| AFW \| VAT percentage is unspecified. Price values will be used \| \| BU_EU_VERK \| Deliveries outside the EU, 0% VAT. \| \| BI_EU_VERK \| Goods inside the EU, 0% VAT. \| \| BI_EU_VERK_D \| Services inside the EU, 0% VAT. \| \| AFST_VERK \| Distance sales inside the EU, 0% VAT. \| \| LAAG_INK_9 \| For buying with 9% VAT. \| \| HOOG_INK_21 \| For buying with 21% VAT. \| \| VERL_INK \| For buying with reverse-charging VAT. \| \| AFW_VERK \| For selling with unspecified VAT percentage. Price values will be used. \| \| BU_EU_INK \| For buying goods/services from outside the EU, 0% VAT. \| \| BI_EU_INK \| For buying goods/services from inside the EU, 0% VAT. \| \| GEEN \| No VAT. \| |
| `rows[].vatAmount` | body | `number` | no | The VAT amount of the row. Only use in combination with vatCode: 'AFW_VERK' or 'AFW'. Only applicable for NL. |
| `rows[].costCenterId` | body | `number` | no | The cost center id of the row. |
| `rows[].amount` | body | `number` | yes | The amount of the row. This value includes or excludes VAT depending on the `inExVat` value of the mutation. |
| `rows[].description` | body | `string` | no | The description of the row. |
| `rows[].invoiceNumber` | body | `string` | no | The invoice number of the row. Required for type 'Invoice payment received' and 'Invoice payment sent'. Error codes MUT_115 Invoice not found. MUT_120 Invoice number is missing. |
| `rows[].relationId` | body | `number` | no | The relation id of the row. Error codes MUT_112 Relation is missing. MUT_113 Relation not found. |
