# Update User Contact with EHS Insight

Warning: This endpoint doesn't allow partial updates, you need to pass all values to avoid data loss

## Endpoint

- **Method:** `POST`
- **Path:** `/v6/entity/UserContact/update`
- **Base URL:** `https://{companyName}.ehsinsight.com/api`
- **Official documentation:** [Update User Contact](https://equixinctest.ehsinsight.com/openapi/viewer?version=6&category=entity)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `RowUID` | body | `string` | yes | The provider RowUID of the user contact to update. |
| `ChangeToken` | body | `string` | no | — |
| `UserContactNumber` | body | `string` | no | — |
| `UserContactType` | body | `string` | no | — |
| `FullName` | body | `string` | no | — |
| `IsEnabled` | body | `number` | no | — |
| `FirstName` | body | `string` | no | — |
| `LastName` | body | `string` | no | — |
| `Gender` | body | `string` | no | — |
| `BirthDate` | body | `string` | no | format example: "2026-04-28" |
| `BusinessEntity` | body | `string` | no | — |
| `Employer` | body | `string` | no | — |
| `Position` | body | `string` | no | — |
| `EmployeeID` | body | `string` | no | — |
| `HireDate` | body | `string` | no | format example: "2026-04-28" |
| `PositionStartDate` | body | `string` | no | format example: "2026-04-28" |
| `IndustryStartDate` | body | `string` | no | format example: "2026-04-28" |
| `HomeAddress` | body | `string` | no | — |
| `HomeCity` | body | `string` | no | — |
| `HomeState` | body | `string` | no | — |
| `HomeZip` | body | `string` | no | — |
| `PhoneNumber` | body | `string` | no | — |
| `Username` | body | `string` | no | — |
| `AuthProvider` | body | `string` | no | — |
| `EmailAddress` | body | `string` | no | — |
| `Supervisor` | body | `string` | no | — |
| `InviteSent` | body | `number` | no | — |
| `UserContactPhoto` | body | `string` | no | — |
| `UDFPersonalCellPhone` | body | `string` | no | — |
| `UDFEmploymentType` | body | `string` | no | — |
| `Udfcdl` | body | `number` | no | — |
| `UDFDriversLicense` | body | `string` | no | — |
| `UDFDriversLicenseExpira` | body | `string` | no | format example: "2026-04-28" |
| `UDFLCACellPhoneNumber` | body | `string` | no | — |
| `UDFOfficePhone` | body | `string` | no | — |
| `UDFTerminationDate` | body | `string` | no | format example: "2026-04-28" |
| `MobilePhoneNumber` | body | `string` | no | — |
| `UserContactPhotoAttachmentUID` | body | `string` | no | — |
| `UserContactPhotoContentType` | body | `string` | no | — |
| `UserContactPhotoFileSize` | body | `string` | no | — |
| `Language` | body | `string` | no | — |
| `LanguageOther` | body | `string` | no | — |
| `UIMode` | body | `string` | no | — |
| `UIModeOther` | body | `string` | no | — |
| `GenderOther` | body | `string` | no | — |
| `PositionOther` | body | `string` | no | — |
| `UDFEmploymentTypeOther` | body | `string` | no | — |
| `EmployerOther` | body | `string` | no | — |
| `AuthProviderOther` | body | `string` | no | — |
| `UserContactPhotoPreviousVersions[]` | body | `array` | no | — |
| `RoleAssignmentType` | body | `string` | no | — |
| `SecurityGroups[]` | body | `array` | no | — |
| `UserRoles[]` | body | `array` | no | — |
