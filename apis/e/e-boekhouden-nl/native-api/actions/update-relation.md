# Update Relation with e-Boekhouden.nl

Updates a relation in e-Boekhouden.nl.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/v1/relation/:id`
- **Base URL:** `https://api.e-boekhouden.nl`
- **API:** rest
- **Official documentation:** [Update Relation](https://api.e-boekhouden.nl/swagger/index.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | — |
| `type` | body | `string` | no | Business (`B`) or Private (`P`). Defaults to `B` if empty. Error codes REL_001 Relation type is invalid (B,P). Maximum length: 1. |
| `code` | body | `string` | no | The code of the relation. Auto-generated if empty. Error codes REL_049 Code already exists. REL_005 Code is invalid. REL_006 Code is too long. Maximum length: 15. |
| `name` | body | `string` | yes | The (company) name of the relation. Error codes REL_002 Name is mandatory. REL_003 Name is too long. Maximum length: 100. |
| `salutation` | body | `string` | no | The salutation of the relation. Error codes REL_010 Salutation is too long. Maximum length: 50. |
| `contact` | body | `string` | no | The contact of the relation. Error codes REL_009 Contact is too long. Maximum length: 50. |
| `gender` | body | `string` | no | Male (`m`) or female (`v`) or department (`a`) Error codes REL_004 Gender is invalid (m,v,a). Maximum length: 1. |
| `address` | body | `string` | no | The primary address of the relation. Error codes REL_011 Address is too long. Maximum length: 150. |
| `postalCode` | body | `string` | no | The primary postal code of the relation. Error codes REL_012 Postal code is too long. Maximum length: 50. |
| `city` | body | `string` | no | The primary city of the relation. Error codes REL_013 City is too long. Maximum length: 50. |
| `country` | body | `string` | no | The primary country of the relation. Error codes REL_014 Country is too long. Maximum length: 50. |
| `address2` | body | `string` | no | The secondary address of the relation. Error codes REL_015 Address 2 is too long. Maximum length: 150. |
| `postalCode2` | body | `string` | no | The secondary postal code of the relation. Error codes REL_016 Postal code 2 is too long. Maximum length: 50. |
| `city2` | body | `string` | no | The secondary city of the relation. Error codes REL_017 City 2 is too long. Maximum length: 50. |
| `country2` | body | `string` | no | The secondary country of the relation. Error codes REL_018 Country 2 is too long. Maximum length: 50. |
| `phoneNumber` | body | `string` | no | The phone number of the relation. Error codes REL_019 Phone is too long. Maximum length: 50. |
| `mobilePhoneNumber` | body | `string` | no | The mobile phone number of the relation. Error codes REL_020 Mobile is too long. Maximum length: 50. |
| `faxNumber` | body | `string` | no | The fax number of the relation. Error codes REL_021 Fax is too long. Maximum length: 50. |
| `emailAddress` | body | `string` | no | The email address of the relation. Error codes REL_022 Email is too long. REL_023 Email is invalid. Maximum length: 150. |
| `emailAddressInvoice` | body | `string` | no | The invoice email address of the relation. Error codes REL_024 Email invoice is too long. REL_025 Email invoice is invalid. Maximum length: 150. |
| `emailAddressReminder` | body | `string` | no | The reminder email address of the relation. Error codes REL_026 Email reminder is too long. REL_027 Email reminder is invalid. Maximum length: 150. |
| `website` | body | `string` | no | The website of the relation. Error codes REL_028 Website is too long. Maximum length: 50. |
| `note` | body | `string` | no | The note of the relation. Maximum length: 40000. |
| `vatNumber` | body | `string` | no | The VAT number of the relation. Error codes REL_035 VAT number is too long. Maximum length: 50. |
| `inactive` | body | `boolean` | no | Whether the relation is inactive. |
| `termOfPayment` | body | `number` | no | The payment term of the relation. Error codes REL_030 Term of payment too low. REL_031 Term of payment too high. |
| `companyRegistrationNumber` | body | `string` | no | The company registration number of the relation. Error codes REL_008 Company registration number must be numeric. REL_050 Company registration number is too long. Maximum length: 50. |
| `iban` | body | `string` | no | The IBAN number of the relation. Error codes REL_007 Iban is invalid. REL_029 Iban is too long. Maximum length: 50. |
| `bic` | body | `string` | no | The BIC number of the relation. Error codes REL_032 BIC is too long. Maximum length: 20. |
| `freeText1` | body | `string` | no | Free text field for the relation. Error codes REL_037 Free text 1 is too long. Maximum length: 100. |
| `freeText2` | body | `string` | no | Free text field for the relation. Error codes REL_038 Free text 2 is too long. Maximum length: 100. |
| `freeText3` | body | `string` | no | Free text field for the relation. Error codes REL_039 Free text 3 is too long. Maximum length: 100. |
| `freeText4` | body | `string` | no | Free text field for the relation. Error codes REL_040 Free text 4 is too long. Maximum length: 100. |
| `freeText5` | body | `string` | no | Free text field for the relation. Error codes REL_041 Free text 5 is too long. Maximum length: 100. |
| `freeText6` | body | `string` | no | Free text field for the relation. Error codes REL_042 Free text 6 is too long. Maximum length: 100. |
| `freeText7` | body | `string` | no | Free text field for the relation. Error codes REL_043 Free text 7 is too long. Maximum length: 100. |
| `freeText8` | body | `string` | no | Free text field for the relation. Error codes REL_044 Free text 8 is too long. Maximum length: 100. |
| `freeText9` | body | `string` | no | Free text field for the relation. Error codes REL_045 Free text 9 is too long. Maximum length: 100. |
| `freeText10` | body | `string` | no | Free text field for the relation. Error codes REL_046 Free text 10 is too long. Maximum length: 100. |
| `doNotReceiveNewsletters` | body | `boolean` | no | Whether the relation will receive newsletters or not. |
| `ledgerId` | body | `number` | no | The ledger ID of this relation. Error codes REL_048 Ledger not found. |
| `mandate` | body | `boolean` | no | Enable or disable mandate. |
| `mandateType` | body | `string` | no | one-time (`E`) or continuous (`D`) Error codes REL_033 Mandate type is too long. REL_051 Mandate type is invalid (E,D). Maximum length: 1. |
| `mandateId` | body | `string` | no | The mandate ID of this relation. Error codes REL_034 Mandate ID is too long. Maximum length: 35. |
