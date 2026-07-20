# Restore Archived Department with FuseDesk

Restores an archived department in FuseDesk.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v2/departments/:departmentId/restore`
- **Base URL:** `https://{appName}.fusedesk.com`
- **Official documentation:** [Restore Archived Department](https://documenter.getpostman.com/view/11014835/SztBc8ix#812e436f-6c89-430e-8ebc-35c3caff62d9)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `departmentId` | path | `number` | yes | The FuseDesk department ID. |
