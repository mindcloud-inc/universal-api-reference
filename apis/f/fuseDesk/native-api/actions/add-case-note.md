# Add Case Note with FuseDesk

Creates a note on an existing FuseDesk case.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/cases/:caseId/addnote`
- **Base URL:** `https://{appName}.fusedesk.com`
- **Official documentation:** [Add Case Note](https://documenter.getpostman.com/view/11014835/SztBc8ix#148b96a5-d816-41d4-ad33-a29642287c85)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `caseId` | path | `number` | yes |
| `note` | body | `string` | yes |
| `repid` | body | `number` | no |
| `status` | body | `string` | no |
| `templateid` | body | `number` | no |
| `title` | body | `string` | no |
| `type` | body | `string` | no |
