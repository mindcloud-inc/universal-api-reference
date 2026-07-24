# Update Payment Supplier with Rillion Prime Pay

## Endpoint

- **Method:** `PUT`
- **Path:** `/payment/supplier`
- **Base URL:** `{baseUrl}`
- **Official documentation:** [Update Payment Supplier](https://prime-2-uat-14-ue.rillionprime.com/swagger/index.html?urls.primaryName=Pay%20-%20v1.0)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `X-Correlation-ID` | header | `string` | no | — |
| `supplierId` | body | `string` | yes | Unique supplier Id Format: `uuid`. |
| `syncWithPaymentProvider` | body | `boolean` | yes | Boolean indicator to decide if Supplier needs to sync with payment provider |
| `supplierstatus` | body | `list<string>` | no | Status of the supplier Accepted values: `PayDisabled`, `PayEnabled`, `RemitAddressNeeded`. |
| `supplierRemitAddress` | body | `object` | no | Remit address for the supplier |
| `supplierPaymentGrouping` | body | `list<list>` | no | Payment grouping option for the supplier Accepted values: `Bundle`, `SendIndividually`. |
| `supplierRemitAddress.street1` | body | `string` | no | Street address line 1 |
| `isInternational` | body | `boolean` | no | Indicates if the supplier is an international supplier |
| `supplierRemitAddress.street2` | body | `string` | no | Street address line 2 |
| `internationalDetails` | body | `object` | no | International payment details for the supplier |
| `supplierRemitAddress.postalCode` | body | `string` | no | Postal Code |
| `supplierRemitAddress.zipCode` | body | `string` | no | Zip Code |
| `supplierRemitAddress.city` | body | `string` | no | City |
| `supplierRemitAddress.state` | body | `string` | no | State |
| `supplierRemitAddress.country` | body | `string` | no | Country |
| `supplierRemitAddress.careOf` | body | `string` | no | CareOf |
| `internationalDetails.currency` | body | `string` | no | Currency code |
| `internationalDetails.iban` | body | `string` | no | International Bank Account Number |
| `internationalDetails.swift` | body | `string` | no | SWIFT/BIC code |
| `internationalDetails.accountNumber` | body | `string` | no | Bank account number |
| `internationalDetails.routingCode` | body | `string` | no | Routing code |
| `internationalDetails.clabe` | body | `string` | no | CLABE number (Mexico) |
| `internationalDetails.bankName` | body | `string` | no | Name of the bank |
| `internationalDetails.bankCountry` | body | `string` | no | Country of the bank |
| `internationalDetails.remittanceEmail` | body | `string` | no | Email for remittance advice |
| `internationalDetails.phoneNo` | body | `string` | no | Phone number |
| `internationalDetails.payeeType` | body | `string` | no | Type of payee |
| `internationalDetails.purpose` | body | `string` | no | Purpose of payment |
| `internationalDetails.branchCode` | body | `string` | no | Branch code |
| `internationalDetails.accountType` | body | `string` | no | Account type |
