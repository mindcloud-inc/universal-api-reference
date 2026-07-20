# Update company position with Doyle HCM

Updates a company position in Doyle HCM.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/wep/companies/:companyId/positions/:positionId`
- **Base URL:** `https://api.worklio.com`
- **Official documentation:** [Update company position](https://apidocs.worklio.com/reference/patch_wep-companies-companyid-positions-positionid)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `companyId` | path | `number` | yes |
| `positionId` | path | `number` | yes |
| `name` | body | `string` | yes |
| `code` | body | `string` | yes |
| `defaultRate` | body | `number` | no |
| `defaultWCCode` | body | `string` | no |
| `rate` | body | `object` | no |
| `annualSalary` | body | `object` | no |
