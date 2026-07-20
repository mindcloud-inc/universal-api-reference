# Update company department with Doyle HCM

Updates a company department in Doyle HCM.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/wep/companies/:companyId/departments/:departmentId`
- **Base URL:** `https://api.worklio.com`
- **Official documentation:** [Update company department](https://apidocs.worklio.com/reference/patch_wep-companies-companyid-departments-departmentid)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `companyId` | path | `number` | yes |
| `departmentId` | path | `number` | yes |
| `name` | body | `string` | yes |
| `phone` | body | `string` | no |
| `ext` | body | `string` | no |
| `managerId` | body | `number` | no |
