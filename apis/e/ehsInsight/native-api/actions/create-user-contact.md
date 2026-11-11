# Create User Contact with EHS Insight

## Endpoint

- **Method:** `POST`
- **Path:** `/v6/entity/UserContact/add`
- **Base URL:** `https://{companyName}.ehsinsight.com/api`
- **Official documentation:** [Create User Contact](https://qxobptest.ehsinsight.com/site#/apidocumentation/v6/apidoc_entityapi_add)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `UserContactType` | body | `list<string>` | no | Use User to create a login account or Contact to create a contact. Other types depend on your site's configuration. Accepted values: `Contact`, `Device`, `Guest`, `Kiosk`, `Template`, `Unmanaged`, `User`. |
| `FullName` | body | `string` | no | — |
| `IsEnabled` | body | `number` | no | — |
| `AuthProvider` | body | `string` | no | Authentication provider for a User account. API version 6 uses Password for password authentication. |
| `Username` | body | `string` | no | — |
| `EmailAddress` | body | `string` | no | — |
| `FirstName` | body | `string` | no | — |
| `LastName` | body | `string` | no | — |
| `BusinessEntity` | body | `string` | no | — |
| `Employer` | body | `string` | no | — |
| `Position` | body | `string` | no | — |
| `EmployeeID` | body | `string` | no | — |
| `RoleAssignmentType` | body | `string` | no | For users, use DirectAssignment with User Roles or SecurityGroups with Security Groups. Supply the matching role or group collection. |
| `UserRoles[]` | body | `array<object>` | no | — |
| `UserRoles[].RoleUID` | body | `string` | no | — |
| `UserRoles[].BusinessEntity` | body | `string` | no | — |
| `SecurityGroups[]` | body | `array<object>` | no | — |
| `SecurityGroups[].SecurityGroup` | body | `string` | no | — |
| `SecurityGroups[].Parameters[]` | body | `array<object>` | no | — |
| `SecurityGroups[].Parameters[].TemplateParameter` | body | `string` | no | — |
| `SecurityGroups[].Parameters[].BusinessEntities[]` | body | `array<object>` | no | — |
| `SecurityGroups[].Parameters[].BusinessEntities[].Item` | body | `string` | no | — |
