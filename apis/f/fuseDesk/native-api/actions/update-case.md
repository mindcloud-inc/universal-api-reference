# Update Case with FuseDesk

Updates an existing case in FuseDesk.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/cases/:caseId`
- **Base URL:** `https://{appName}.fusedesk.com`
- **Official documentation:** [Update Case](https://documenter.getpostman.com/view/11014835/SztBc8ix#62bfa40e-747e-4b05-97cf-c15e84ffe55d)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `caseId` | path | `number` | yes |
| `companyid` | body | `number` | no |
| `contactid` | body | `number` | no |
| `contactUuid` | body | `string` | no |
| `depid` | body | `number` | no |
| `details` | body | `string` | no |
| `repid` | body | `number` | no |
| `status` | body | `string` | no |
| `summary` | body | `string` | no |
