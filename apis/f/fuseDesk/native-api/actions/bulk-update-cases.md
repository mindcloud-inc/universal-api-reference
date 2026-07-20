# Bulk Update Cases with FuseDesk

Updates multiple existing cases in FuseDesk.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/cases/update`
- **Base URL:** `https://{appName}.fusedesk.com`
- **Official documentation:** [Bulk Update Cases](https://documenter.getpostman.com/view/11014835/SztBc8ix#be7213cd-a217-4953-9090-7095216f3356)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `caseids` | query | `string` | yes |
| `crmAutomationId` | query | `number` | no |
| `crmTagId` | query | `number` | no |
| `depid` | query | `number` | no |
| `merge` | query | `boolean` | no |
| `repid` | query | `number` | no |
| `snooze` | query | `string` | no |
| `status` | query | `string` | no |
| `tagid` | query | `number` | no |
