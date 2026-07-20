# Create Case with FuseDesk

Creates a new case in FuseDesk.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/cases`
- **Base URL:** `https://{appName}.fusedesk.com`
- **Official documentation:** [Create Case](https://documenter.getpostman.com/view/11014835/SztBc8ix#760ba74c-07f2-4f43-a057-b0417d12e694)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `casetags` | body | `string` | no |
| `companyid` | body | `number` | no |
| `contactid` | body | `number` | no |
| `contactUuid` | body | `string` | no |
| `date_assigned` | body | `string` | no |
| `date_opened` | body | `string` | no |
| `depid` | body | `number` | yes |
| `details` | body | `string` | yes |
| `openedby` | body | `string` | yes |
| `repid` | body | `number` | no |
| `status` | body | `string` | no |
| `summary` | body | `string` | yes |
