# Create Meeting with Teachlr Organizations

## Endpoint

- **Method:** `POST`
- **Path:** `/meetings`
- **Base URL:** `https://api.teachlr.com/mindcloudteachlr337933/api`
- **Official documentation:** [Create Meeting](https://soporte.teachlr.com/base-de-conocimientos/creacion-actualizacion-y-eliminacion-de-videoconferencias-para-un-usuario-de-una-escuela-usando-el-api-de-teachlr-organizaciones-2/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `email` | body | `string` | yes | Email of the user who will host the meeting. |
| `topic` | body | `string` | yes | Topic of the meeting. |
| `date` | body | `string` | yes | Meeting date in YYYY-MM-DD format. |
| `time` | body | `string` | yes | Meeting start time. |
| `duration` | body | `number` | yes | Meeting duration in minutes. |
| `timezone` | body | `string` | yes | Timezone identifier for the meeting. |
