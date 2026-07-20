# Update Department with FuseDesk

Updates an existing department in FuseDesk.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v2/departments/:departmentId`
- **Base URL:** `https://{appName}.fusedesk.com`
- **Official documentation:** [Update Department](https://documenter.getpostman.com/view/11014835/SztBc8ix#56fca54b-34af-4d3d-9eb5-b5055401b4ac)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `allReps` | body | `boolean` | no | Whether all reps can access the department. |
| `departmentId` | path | `number` | yes | The FuseDesk department ID. |
| `feedbackDelay` | body | `number` | no | Delay before sending feedback. |
| `feedbackFrequency` | body | `number` | no | Feedback request frequency. |
| `feedbackSample` | body | `number` | no | Feedback sample percentage. |
| `feedbackTemplateId` | body | `number` | no | Feedback template ID. |
| `replyTemplateId` | body | `number` | no | Reply template ID. |
| `repUserIds[]` | body | `array<number>` | no | Rep user IDs assigned to the department. |
| `stale` | body | `number` | no | Stale threshold in minutes. |
| `staleWarning` | body | `number` | no | Stale warning threshold in minutes. |
| `templateCategory` | body | `string` | no | Template category label. |
