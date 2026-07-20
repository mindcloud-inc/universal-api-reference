# Set company access policy with Doyle HCM

Updates the company access policy in Doyle HCM.

## Endpoint

- **Method:** `POST`
- **Path:** `/wep/companies/:companyId/access-policy`
- **Base URL:** `https://api.worklio.com`
- **Official documentation:** [Set company access policy](https://apidocs.worklio.com/reference/post_wep-companies-companyid-access-policy)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `companyId` | path | `number` | yes |
| `allowEePortalForEes` | body | `boolean` | yes |
