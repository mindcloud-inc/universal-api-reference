# Update Employee with Viewpoint Vista

## Endpoint

- **Method:** `POST`
- **Path:** `v1/direct/subscribers/{subscriberCode}/vista/pr/2/data/employees/actions/change`
- **Base URL:** `https://api.xchange.trimble.com/connect/`
- **API:** REST
- **Official documentation:** [Update Employee](https://direct-api.xchange.trimble.com/reference/post-directsubscriberssubscriber_codevistapr2dataemployeesactionschange)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `__key` | body | `object` | yes | Required employee key. Provide either Key ID or PR Company and Employee. |
| `__key.KeyID` | body | `number` | no | Employee record key ID. Use this or the PR Company and Employee pair. |
| `__key.PRCo` | body | `number` | no | Payroll company for the employee natural key. Use with Employee when Key ID is not supplied. |
| `__key.Employee` | body | `number` | no | Employee number for the natural key. Use with PR Company when Key ID is not supplied. |
| `SortName` | body | `string` | no | Optional employee sort name. Maximum 15 characters. Maximum length: 15. |
| `LastName` | body | `string` | no | Optional employee last name. Maximum 30 characters. Maximum length: 30. |
| `FirstName` | body | `string` | no | Optional employee first name. Maximum 30 characters. Maximum length: 30. |
| `MidName` | body | `string` | no | Optional employee middle name. Maximum 15 characters. Maximum length: 15. |
| `Suffix` | body | `string` | no | Optional name suffix. Maximum 4 characters. Maximum length: 4. |
| `Address` | body | `string` | no | Optional street address. Maximum 60 characters. Maximum length: 60. |
| `Address2` | body | `string` | no | Optional second address line. Maximum 60 characters. Maximum length: 60. |
| `City` | body | `string` | no | Optional city. Maximum 30 characters. Maximum length: 30. |
| `State` | body | `string` | no | Optional state. Must exist in the selected country’s Vista states. Maximum length: 4. |
| `Zip` | body | `string` | no | Optional postal code. Maximum 12 characters. Maximum length: 12. |
| `Country` | body | `string` | no | Optional country code. Key to Vista countries. Maximum 2 characters. Maximum length: 2. |
| `Email` | body | `string` | no | Optional email address. Maximum 255 characters. Maximum length: 255. |
| `Phone` | body | `string` | no | Optional phone number. Maximum 20 characters. Maximum length: 20. |
| `CellPhone` | body | `string` | no | Optional cell phone number. Maximum 20 characters. Maximum length: 20. |
| `SSN` | body | `string` | no | Protected field. Optional Social Security number. Maximum 11 characters. Maximum length: 11. |
| `Race` | body | `string` | no | Protected field. Optional race code. Maximum 2 characters. Maximum length: 2. |
| `Sex` | body | `string` | no | Protected field. Optional code: F or M. Maximum length: 1. |
| `BirthDate` | body | `string` | no | Protected field. Optional date in YYYY-MM-DD format. |
| `Notes` | body | `string` | no | Optional employee notes. |
| `ActiveYN` | body | `string` | no | Optional status. Allowed values: Y or N. |
| `HireDate` | body | `string` | no | Optional date in YYYY-MM-DD format. |
| `TermDate` | body | `string` | no | Optional date in YYYY-MM-DD format. |
| `RecentRehireDate` | body | `string` | no | Optional date in YYYY-MM-DD format. |
| `RecentSeparationDate` | body | `string` | no | Optional date in YYYY-MM-DD format. |
| `NewHireActStartDate` | body | `string` | no | Optional date in YYYY-MM-DD format. |
| `NewHireActEndDate` | body | `string` | no | Optional date in YYYY-MM-DD format. |
| `TimesheetRevGroup` | body | `string` | no | Optional timesheet reviewer group. Maximum 10 characters. Maximum length: 10. |
| `OccupCat` | body | `string` | no | Optional occupational category. Maximum 10 characters. Maximum length: 10. |
| `CatStatus` | body | `string` | no | Optional status: A, J, T, or N. Maximum length: 1. |
| `TradeSeq` | body | `number` | no | Optional CHAMP equal-opportunity trade sequence. |
| `NonResAlienYN` | body | `string` | no | Protected field. Optional Y/N value. Maximum length: 1. |
| `APVendorGroup` | body | `number` | no | Optional AP vendor group. |
| `APVendor` | body | `number` | no | Optional AP vendor. |
| `__custom_fields` | body | `object` | no | Optional Vista user-defined fields, keyed by field name. |
| `PayrollDefaults` | body | `object` | no | Optional payroll defaults object. Send documented fields that need changing. |
| `CurrentJob` | body | `object` | no | Optional current job object. Send documented fields that need changing. |
| `StandardPay` | body | `object` | no | Optional standard pay object. Send documented fields that need changing. |
| `PrimaryDirectDeposit` | body | `object` | no | Optional primary direct deposit object. Send documented fields that need changing. |
| `GarnishmentAllocation` | body | `object` | no | Optional garnishment allocation object. Send documented fields that need changing. |
| `CanadaData` | body | `object` | no | Optional Canada-specific payroll data object. |
| `AustraliaData` | body | `object` | no | Optional Australia-specific payroll data object. |
