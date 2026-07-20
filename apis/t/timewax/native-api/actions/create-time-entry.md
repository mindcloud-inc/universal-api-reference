# Create Time Entry with Timewax

Creates a new time entry in Timewax.

## Endpoint

- **Method:** `POST`
- **Path:** `time/entries/add/`
- **Base URL:** `https://api.timewax.com/`
- **Official documentation:** [Create Time Entry](https://timewax.atlassian.net/rest/servicedesk/knowledgebase/latest/articles/view/2231664899)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `resource` | body | `string` | yes | Required. Code or name of the resource. |
| `project` | body | `string` | yes | Required. Code or name of the project. |
| `breakdown` | body | `string` | yes | Required. Code or name of the activity. |
| `date` | body | `date` | yes | Required. Date of the booking, format yyyymmdd or yyyy-mm-dd. |
| `hours` | body | `number` | yes | Required. Number of hours. |
| `startTime` | body | `string` | yes | Required. Start time of the time line, format hh:mm. |
| `endTime` | body | `string` | yes | Required. End time of the time line, format hh:mm. |
