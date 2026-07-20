# Create company position with Doyle HCM

Creates a company position in Doyle HCM.

## Endpoint

- **Method:** `POST`
- **Path:** `/wep/companies/:companyId/positions`
- **Base URL:** `https://api.worklio.com`
- **Official documentation:** [Create company position](https://apidocs.worklio.com/reference/post_wep-companies-companyid-positions)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `companyId` | path | `number` | yes |
| `name` | body | `string` | yes |
| `code` | body | `string` | yes |
| `defaultRate` | body | `number` | no |
| `defaultWCCode` | body | `string` | no |
| `rate` | body | `object` | no |
| `annualSalary` | body | `object` | no |
