# Update Payment Suppliers with Rillion Prime Pay

## Endpoint

- **Method:** `PUT`
- **Path:** `/payment/suppliers`
- **Base URL:** `{baseUrl}`
- **Official documentation:** [Update Payment Suppliers](https://prime-2-uat-14-ue.rillionprime.com/swagger/index.html?urls.primaryName=Pay%20-%20v1.0)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `suppliers[]` | body | `array<object>` | yes | Array of suppliers to update |
| `suppliers[].supplierId` | body | `string` | yes | Unique supplier Id |
| `suppliers[].syncWithPaymentProvider` | body | `boolean` | yes | Boolean indicator to decide if Supplier needs to sync with payment provider |
| `suppliers[].supplierstatus` | body | `list<string>` | no | Status of the supplier Accepted values: `PayDisabled`, `PayEnabled`, `RemitAddressNeeded`. |
| `suppliers[].supplierRemitAddress` | body | `object` | no | Remit address for the supplier |
| `suppliers[].supplierRemitAddress.street1` | body | `string` | no | Street address line 1 |
| `suppliers[].supplierRemitAddress.street2` | body | `string` | no | Street address line 2 |
| `suppliers[].supplierRemitAddress.postalCode` | body | `string` | no | Postal Code |
| `suppliers[].supplierRemitAddress.zipCode` | body | `string` | no | Zip Code |
| `suppliers[].supplierRemitAddress.city` | body | `string` | no | City |
| `suppliers[].supplierRemitAddress.state` | body | `string` | no | State |
| `suppliers[].supplierRemitAddress.country` | body | `string` | no | Country |
| `suppliers[].supplierRemitAddress.careOf` | body | `string` | no | CareOf |
| `suppliers[].supplierPaymentGrouping` | body | `list<string>` | no | Payment grouping option for the supplier Accepted values: `Bundle`, `SendIndividually`. |
| `suppliers[].isInternational` | body | `boolean` | no | Indicates if the supplier is an international supplier |
| `suppliers[].internationalDetails` | body | `object` | no | International payment details for the supplier |
| `suppliers[].internationalDetails.currency` | body | `string` | no | Currency code |
| `suppliers[].internationalDetails.iban` | body | `string` | no | International Bank Account Number |
| `suppliers[].internationalDetails.swift` | body | `string` | no | SWIFT/BIC code |
| `suppliers[].internationalDetails.accountNumber` | body | `string` | no | Bank account number |
| `suppliers[].internationalDetails.routingCode` | body | `string` | no | Routing code |
| `suppliers[].internationalDetails.clabe` | body | `string` | no | CLABE number (Mexico) |
| `suppliers[].internationalDetails.bankName` | body | `string` | no | Name of the bank |
| `suppliers[].internationalDetails.bankCountry` | body | `string` | no | Country of the bank |
| `suppliers[].internationalDetails.remittanceEmail` | body | `string` | no | Email for remittance advice |
| `suppliers[].internationalDetails.phoneNo` | body | `string` | no | Phone number |
| `suppliers[].internationalDetails.payeeType` | body | `string` | no | Type of payee |
| `suppliers[].internationalDetails.purpose` | body | `string` | no | Purpose of payment |
