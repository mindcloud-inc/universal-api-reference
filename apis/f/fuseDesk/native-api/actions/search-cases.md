# Search Cases with FuseDesk

Finds cases in FuseDesk by matching search filters.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v1/cases`
- **Base URL:** `https://{appName}.fusedesk.com`
- **Official documentation:** [Search Cases](https://documenter.getpostman.com/view/11014835/SztBc8ix#312f3a20-e8bb-4bff-a73e-b9d075ced263)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `companyid` | query | `string` | no |
| `contactid` | query | `string` | no |
| `contactUuid` | query | `string` | no |
| `createdByRep` | query | `string` | no |
| `date_assigned` | query | `string` | no |
| `date_closed` | query | `string` | no |
| `date_firstresponse` | query | `string` | no |
| `date_opened` | query | `string` | no |
| `date_updated` | query | `string` | no |
| `depid` | query | `string` | no |
| `email` | query | `string` | no |
| `from` | query | `string` | no |
| `limit` | query | `string` | no |
| `offset` | query | `string` | no |
| `orderby` | query | `string` | no |
| `repid` | query | `string` | no |
| `status` | query | `string` | no |
| `subject` | query | `string` | no |
