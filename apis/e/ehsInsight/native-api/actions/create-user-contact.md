# Create User Contact with EHS Insight

## Endpoint

- **Method:** `POST`
- **Path:** `/v6/entity/UserContact/add`
- **Base URL:** `https://{companyName}.ehsinsight.com/api`
- **Official documentation:** [Create User Contact](https://equixinctest.ehsinsight.com/openapi/viewer?version=6&category=entity)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `UserContactType` | body | `list` | no |
| `FullName` | body | `string` | no |
| `IsEnabled` | body | `number` | no |
| `AuthProvider` | body | `string` | no |
| `Username` | body | `string` | no |
| `EmailAddress` | body | `string` | no |
| `FirstName` | body | `string` | no |
| `LastName` | body | `string` | no |
| `BusinessEntity` | body | `string` | no |
| `Employer` | body | `string` | no |
| `Position` | body | `string` | no |
| `EmployeeID` | body | `string` | no |
| `RoleAssignmentType` | body | `string` | no |
| `UserRoles[]` | body | `array<object>` | no |
| `UserRoles[].RoleUID` | body | `string` | no |
| `UserRoles[].BusinessEntity` | body | `string` | no |
| `SecurityGroups[]` | body | `array<object>` | no |
| `SecurityGroups[].SecurityGroup` | body | `string` | no |
| `SecurityGroups[].Parameters[]` | body | `array<object>` | no |
| `SecurityGroups[].Parameters[].TemplateParameter` | body | `string` | no |
| `SecurityGroups[].Parameters[].BusinessEntities[]` | body | `array<object>` | no |
| `SecurityGroups[].Parameters[].BusinessEntities[].Item` | body | `string` | no |
