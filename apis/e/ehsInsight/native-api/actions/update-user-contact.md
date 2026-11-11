# Update User Contact with EHS Insight

## Endpoint

- **Method:** `POST`
- **Path:** `/v6/entity/UserContact/update`
- **Base URL:** `https://{companyName}.ehsinsight.com/api`
- **Official documentation:** [Update User Contact](https://qxobptest.ehsinsight.com/site#/apidocumentation/v6/apidoc_entityapi_update)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `RowUID` | body | `string` | yes | RowUID from Get User Contact. |
| `ChangeToken` | body | `string` | yes | Use the unchanged ChangeToken from the freshly fetched full record. |
| `UserContactNumber` | body | `string` | no | Preserve the fetched value. |
| `UserContactType` | body | `string` | no | Preserve the fetched value. Do not reset a user to Contact when an administrator has converted the record. |
| `FullName` | body | `string` | no | — |
| `IsEnabled` | body | `number` | no | Preserve the fetched numeric value unless changing enabled status intentionally. |
| `FirstName` | body | `string` | no | — |
| `LastName` | body | `string` | no | — |
| `Gender` | body | `string` | no | — |
| `BirthDate` | body | `date` | no | — |
| `BusinessEntity` | body | `string` | no | RowUID of the business entity. |
| `Employer` | body | `string` | no | RowUID from the Employer entity list. |
| `Position` | body | `string` | no | RowUID from the Position entity list. |
| `EmployeeID` | body | `string` | no | — |
| `HireDate` | body | `date` | no | — |
| `PositionStartDate` | body | `date` | no | — |
| `IndustryStartDate` | body | `date` | no | — |
| `HomeAddress` | body | `string` | no | — |
| `HomeCity` | body | `string` | no | — |
| `HomeState` | body | `string` | no | — |
| `HomeZip` | body | `string` | no | — |
| `PhoneNumber` | body | `string` | no | — |
| `AuthProvider` | body | `string` | no | Preserve the fetched authentication provider. API version 6 uses Password for password authentication. |
| `Username` | body | `string` | no | — |
| `EmailAddress` | body | `string` | no | — |
| `RoleAssignmentType` | body | `string` | no | Preserve the fetched role assignment mode: DirectAssignment uses User Roles; SecurityGroups uses Security Groups. |
| `UserRoles[]` | body | `array<object>` | no | Preserve the complete fetched direct-role assignments. |
| `UserRoles[].RoleUID` | body | `string` | no | — |
| `UserRoles[].BusinessEntity` | body | `string` | no | Role-scoped Business Entity. Preserve null for roles that apply across all entities. |
| `SecurityGroups[]` | body | `array<object>` | no | Preserve the complete fetched group assignments and parameters. |
| `SecurityGroups[].SecurityGroup` | body | `string` | no | — |
| `SecurityGroups[].Parameters[]` | body | `array<object>` | no | — |
| `SecurityGroups[].Parameters[].TemplateParameter` | body | `string` | no | — |
| `SecurityGroups[].Parameters[].BusinessEntities[]` | body | `array<object>` | no | — |
| `SecurityGroups[].Parameters[].BusinessEntities[].Item` | body | `string` | no | — |
