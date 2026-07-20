# Create Member with e-Boekhouden.nl

Creates a new member in e-Boekhouden.nl.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/member`
- **Base URL:** `https://api.e-boekhouden.nl`
- **API:** rest
- **Official documentation:** [Create Member](https://api.e-boekhouden.nl/swagger/index.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `memberNumber` | body | `string` | no | The code of the member. Auto-generated if empty. Error codes MEM_049 Member number already exists. MEM_005 Member number is invalid. MEM_006 Member number is too long. Maximum length: 15. |
| `name` | body | `string` | yes | The name of the member. Error codes MEM_002 Name is mandatory. MEM_003 Name is too long. Maximum length: 100. |
| `salutation` | body | `string` | no | The salutation of the member. Error codes MEM_010 Salutation is too long. Maximum length: 50. |
| `gender` | body | `string` | no | Male (`m`), female (`v`) or department ('a') Error codes MEM_004 Gender is invalid (m,v,a). Maximum length: 1. |
| `address` | body | `string` | no | The primary address of the member. Error codes MEM_011 Address is too long. Maximum length: 150. |
| `postalCode` | body | `string` | no | The primary postal code of the member. Error codes MEM_012 Postal code is too long. Maximum length: 50. |
| `city` | body | `string` | no | The primary city of the member. Error codes MEM_013 City is too long. Maximum length: 50. |
| `country` | body | `string` | no | The primary country of the member. Error codes MEM_014 Country is too long. Maximum length: 50. |
| `phoneNumber` | body | `string` | no | The phone number of the member. Error codes MEM_019 Phone is too long. Maximum length: 50. |
| `mobilePhoneNumber` | body | `string` | no | The mobile phone number of the member. Error codes MEM_020 Mobile is too long. Maximum length: 50. |
| `faxNumber` | body | `string` | no | The fax number of the member. Error codes MEM_021 Fax is too long. Maximum length: 50. |
| `emailAddress` | body | `string` | no | The email address of the member. Error codes MEM_022 Email is too long. MEM_023 Email is invalid. Maximum length: 150. |
| `emailAddressInvoice` | body | `string` | no | The invoice email address of the member. Error codes MEM_024 Email invoice is too long. MEM_025 Email invoice is invalid. Maximum length: 150. |
| `emailAddressReminder` | body | `string` | no | The reminder email address of the member. Error codes MEM_026 Email reminder is too long. MEM_027 Email reminder is invalid. Maximum length: 150. |
| `note` | body | `string` | no | The note of the member. Maximum length: 40000. |
| `termOfPayment` | body | `number` | no | The payment term of the member. Error codes MEM_030 Term of payment too low. MEM_031 Term of payment too high. |
| `iban` | body | `string` | no | The IBAN number of the member. Error codes MEM_007 Iban is invalid. MEM_029 Iban is too long. Maximum length: 50. |
| `bic` | body | `string` | no | The BIC number of the member. Error codes MEM_032 BIC is too long. Maximum length: 20. |
| `freeText1` | body | `string` | no | Free text field for the member. Error codes MEM_037 Free text 1 is too long. Maximum length: 100. |
| `freeText2` | body | `string` | no | Free text field for the member. Error codes MEM_038 Free text 2 is too long. Maximum length: 100. |
| `freeText3` | body | `string` | no | Free text field for the member. Error codes MEM_039 Free text 3 is too long. Maximum length: 100. |
| `freeText4` | body | `string` | no | Free text field for the member. Error codes MEM_040 Free text 4 is too long. Maximum length: 100. |
| `freeText5` | body | `string` | no | Free text field for the member. Error codes MEM_041 Free text 5 is too long. Maximum length: 100. |
| `freeText6` | body | `string` | no | Free text field for the member. Error codes MEM_042 Free text 6 is too long. Maximum length: 100. |
| `freeText7` | body | `string` | no | Free text field for the member. Error codes MEM_043 Free text 7 is too long. Maximum length: 100. |
| `freeText8` | body | `string` | no | Free text field for the member. Error codes MEM_044 Free text 8 is too long. Maximum length: 100. |
| `freeText9` | body | `string` | no | Free text field for the member. Error codes MEM_045 Free text 9 is too long. Maximum length: 100. |
| `freeText10` | body | `string` | no | Free text field for the member. Error codes MEM_046 Free text 10 is too long. Maximum length: 100. |
| `doNotReceiveNewsletters` | body | `boolean` | no | Whether the member will receive newsletters or not. |
| `ledgerId` | body | `number` | no | The ledger ID of this member. Error codes MEM_048 Ledger not found. |
| `mandate` | body | `boolean` | no | Enable or disable mandate. |
| `mandateType` | body | `string` | no | one-time (`E`) or continuous (`D`) Error codes MEM_033 Mandate type is too long. MEM_051 Mandate type is invalid (E,D). Maximum length: 1. |
| `mandateId` | body | `string` | no | The mandate ID of this member. Error codes MEM_034 Mandate ID is too long. Maximum length: 35. |
