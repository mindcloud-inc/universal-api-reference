# Create Invoice with e-Boekhouden.nl

Creates a new invoice in e-Boekhouden.nl.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/invoice`
- **Base URL:** `https://api.e-boekhouden.nl`
- **API:** rest
- **Official documentation:** [Create Invoice](https://api.e-boekhouden.nl/swagger/index.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `invoiceNumber` | body | `string` | no | Invoice number. Must end with a number. If empty, we will create a new number. Error codes FACT_006 Invoice number is missing. FACT_007 Invoice number is too long. FACT_008 Invoice number is invalid. FACT_009 Invoice number does not end with a digit. FACT_101 Invoice number is in use. Maximum length: 50. |
| `relationId` | body | `number` | yes | The ID of a relation. Error codes FACT_001 Relation ID is missing. FACT_002 Relation not found. FACT_003 Relation is inactive. FACT_EMAIL_001 Relation email is missing. FACT_EMAIL_002 Relation email is invalid. FACT_EMAIL_003 Relation email for invoices is invalid. FACT_EMAIL_004 Relation email for reminders is invalid. FACT_EMAIL_007 Relation email is missing. |
| `date` | body | `date` | no | Invoice date. Error codes FACT_011 Invoice date is missing. FACT_012 Invoice date invalid. FACT_013 Invoice date out of range. |
| `termOfPayment` | body | `number` | yes | Error codes FACT_015 Term of payment is missing. FACT_016 Term of payment out of range. |
| `inExVat` | body | `string` | no | Indicates if the amount on the invoice is including (`IN`) or excluding (`EX`) VAT. The corresponding value will be calculated based on the VAT code. If left empty the 'EX' option will be used Error codes FACT_010 Invoice VAT must be IN or EX. |
| `templateId` | body | `number` | yes | Error codes FACT_018 Invoice template not found. |
| `emailTemplateId` | body | `number` | no | The ID of an email template. Error codes FACT_020 Email template not found. |
| `reference` | body | `string` | no | Reference of the invoice. Error codes FACT_014 Payment reference is too long. Maximum length: 50. |
| `text` | body | `string` | no | Text of the invoice. Error codes FACT_017 Invoice text is too long. Maximum length: 35000. |
| `print` | body | `boolean` | no | Determines whether the invoice should be prepared for printing. |
| `email.fromEmail` | body | `string` | no | Email address of the sender. Error codes FACT_EMAIL_006 Sender email is invalid. |
| `email.fromName` | body | `string` | no | Name of the sender. |
| `email.subject` | body | `string` | no | Email subject. Error codes FACT_EMAIL_013 Subject is missing. |
| `email.body` | body | `string` | no | Email body. Supports HTML. Error codes FACT_EMAIL_011 Email body is too long FACT_EMAIL_014 Body is missing. |
| `email.attachUbl` | body | `boolean` | no | Also attach the invoice UBL-file. |
| `email.invoiceUbl` | body | `boolean` | no | Obsolete; please use `attachUbl` instead. This field will be removed in the future. |
| `directDebit.iban` | body | `string` | yes | Error codes FACT_INCASSO_008 IBAN is missing. FACT_INCASSO_009 IBAN is too long. FACT_INCASSO_010 IBAN is invalid. Maximum length: 150. |
| `directDebit.mandateType` | body | `string` | no | `O` or `E` (one-time debit), `R` or `D` (recurrent debit) Error codes FACT_INCASSO_001 Mandate type is missing. FACT_INCASSO_002 Mandate type is invalid. Maximum length: 1. |
| `directDebit.mandateId` | body | `string` | no | Error codes FACT_INCASSO_003 Mandate ID is missing. FACT_INCASSO_004 Mandate ID is too long. Maximum length: 35. |
| `directDebit.mandateSignedDate` | body | `date` | no | Error codes FACT_INCASSO_005 Mandate signed date is missing. FACT_INCASSO_006 Mandate signed date is invalid. FACT_INCASSO_007 Mandate signed date out of range. |
| `directDebit.name` | body | `string` | no | In the name of. Error codes FACT_INCASSO_011 Name is too long. Maximum length: 150. |
| `directDebit.city` | body | `string` | no | Error codes FACT_INCASSO_012 City is too long. Maximum length: 150. |
| `directDebit.descriptionLine1` | body | `string` | no | Error codes FACT_INCASSO_013 Description line 1 is too long. Maximum length: 50. |
| `directDebit.descriptionLine2` | body | `string` | no | Error codes FACT_INCASSO_014 Description line 2 is too long. Maximum length: 50. |
| `directDebit.descriptionLine3` | body | `string` | no | Error codes FACT_INCASSO_015 Description line 3 is too long. Maximum length: 50. |
| `mutation.description` | body | `string` | no | Description of the mutation. Error codes FACT_VERWERK_002 Description is too long. Maximum length: 200. |
| `mutation.checkPaymentReference` | body | `boolean` | no | If true, the provided `paymentReference` will be validated for uniqueness. |
| `mutation.paymentReference` | body | `string` | no | A reference that uniquely identifies the mutation. Error codes FACT_VERWERK_003 Payment reference is too long. FACT_VERWERK_004 Payment reference already exists. MUTA_008 Payment reference already exists. Maximum length: 50. |
| `mutation.ledgerId` | body | `number` | no | Ledger of the invoice entry. Error codes MUT_007 Unknown ledger for mutation. |
| `items[].quantity` | body | `number` | no | The item quantity, with up to 4 decimal places. |
| `items[].amount` | body | `number` | no | The item quantity. To keep your code ready for future API versions it is recommended to use `quantity` instead. |
| `items[].unitId` | body | `number` | no | The ID of an existing unit. Error codes FACT_ITEM_010 Unit not found. |
| `items[].code` | body | `string` | no | Error codes FACT_ITEM_003 Code invoice item is too long. Maximum length: 50. |
| `items[].productId` | body | `number` | no | The ID of an existing product. If given, `Code` is ignored. Error codes FACT_ITEM_011 Product not found. |
| `items[].description` | body | `string` | yes | Error codes FACT_ITEM_001 Description invoice item is missing. FACT_ITEM_002 Description invoice item is too long. |
| `items[].pricePerUnit` | body | `number` | no | Error codes FACT_ITEM_004 Price per unit excl. VAT is missing. FACT_ITEM_008 Total price is too high. FACT_ITEM_009 Total price is too low. |
| `items[].vatCode` | body | `string` | yes | A list of VAT codes is displayed below. \| Value \| Description \| \|---\|---\| \| HOOG_VERK_21 \| For selling with 21% VAT. \| \| LAAG_VERK_9 \| For selling with 9% VAT. \| \| VERL_VERK \| For selling with reverse-charging 21% VAT. \| \| VERL_VERK_L9 \| For selling with reverse-charging 9% VAT. \| \| AFW \| VAT percentage is unspecified. Price values will be used \| \| BU_EU_VERK \| Deliveries outside the EU, 0% VAT. \| \| BI_EU_VERK \| Goods inside the EU, 0% VAT. \| \| BI_EU_VERK_D \| Services inside the EU, 0% VAT. \| \| AFST_VERK \| Distance sales inside the EU, 0% VAT. \| \| LAAG_INK_9 \| For buying with 9% VAT. \| \| HOOG_INK_21 \| For buying with 21% VAT. \| \| VERL_INK \| For buying with reverse-charging VAT. \| \| AFW_VERK \| For selling with unspecified VAT percentage. Price values will be used. \| \| BU_EU_INK \| For buying goods/services from outside the EU, 0% VAT. \| \| BI_EU_INK \| For buying goods/services from inside the EU, 0% VAT. \| \| GEEN \| No VAT. \| |
| `items[].vatAmount` | body | `number` | no | The VAT amount of the invoice item. Only use in combination with vatCode: 'AFW_VERK'. Only applicable for NL. Error codes FACT_ITEM_015 VAT amount must be used with VAT code: 'AFW_VERK' |
| `items[].ledgerId` | body | `number` | yes | The ID of an existing ledger account Error codes FACT_ITEM_007 Ledger ID is missing FACT_ITEM_012 Ledger account not found. |
| `items[].costCenterId` | body | `number` | no | — |
| `items[].discountAmount` | body | `number` | no | A fixed discount on the `pricePerUnit`. This field can not be combined with `discountPercentage`. |
| `items[].discountPercentage` | body | `number` | no | A percentage discount on the `pricePerUnit`. This field can not be combined with `discountAmount`. |
