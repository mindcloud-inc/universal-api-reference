# Create company department with Doyle HCM

Creates a company department in Doyle HCM.

## Endpoint

- **Method:** `POST`
- **Path:** `/wep/companies/:companyId/departments`
- **Base URL:** `https://api.worklio.com`
- **Official documentation:** [Create company department](https://apidocs.worklio.com/reference/post_wep-companies-companyid-departments)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `companyId` | path | `number` | yes |
| `name` | body | `string` | yes |
| `phone` | body | `string` | no |
| `ext` | body | `string` | no |
| `managerId` | body | `number` | no |
