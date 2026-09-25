# Update Employee with ServiceTitan

Updates an existing employee in ServiceTitan.

## Endpoint

- **Method:** `PATCH`
- **Path:** `settings/v2/tenant/{tenant}/employees/:id`
- **Base URL:** `https://{baseUrl}/`
- **Official documentation:** [Update Employee](https://developer.servicetitan.io/api-details/#api=tenant-settings-v2&operation=Employees_GetList)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `customFields[].typeId` | body | `number` | no |
| `name` | body | `string` | yes |
| `customFields[].name` | body | `string` | no |
| `mobilePhoneNumber` | body | `string` | no |
| `customFields[].value` | body | `string` | no |
| `phoneNumber` | body | `string` | no |
| `email` | body | `string` | yes |
| `login` | body | `string` | no |
| `password` | body | `string` | no |
| `accountCreationMethod` | body | `list<string>` | yes |
| `businessUnitId` | body | `number` | no |
| `roleId` | body | `number` | yes |
| `positions[]` | body | `array<string>` | yes |
| `aadUserId` | body | `string` | no |
| `customFields[]` | body | `array` | no |
| `id` | path | `string` | no |
