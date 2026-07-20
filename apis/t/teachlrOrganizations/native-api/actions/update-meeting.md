# Update Meeting with Teachlr Organizations

## Endpoint

- **Method:** `PUT`
- **Path:** `/meetings/:meetingId`
- **Base URL:** `https://api.teachlr.com/mindcloudteachlr337933/api`
- **Official documentation:** [Update Meeting](https://soporte.teachlr.com/base-de-conocimientos/creacion-actualizacion-y-eliminacion-de-videoconferencias-para-un-usuario-de-una-escuela-usando-el-api-de-teachlr-organizaciones-2/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `date` | body | `string` | no | Updated meeting date. |
| `meeting_id` | path | `string` | yes | Identifier of the meeting to update. |
| `time` | body | `string` | no | Updated meeting time. |
| `timezone` | body | `string` | no | Updated meeting timezone. |
| `topic` | body | `string` | no | Updated topic of the meeting. |
| `duration` | body | `number` | no | Updated meeting duration. |
