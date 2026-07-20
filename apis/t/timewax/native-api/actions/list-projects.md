# List Projects with Timewax

Retrieves all projects from Timewax.

## Endpoint

- **Method:** `POST`
- **Path:** `project/list/`
- **Base URL:** `https://api.timewax.com/`
- **Official documentation:** [List Projects](https://timewax.atlassian.net/rest/servicedesk/knowledgebase/latest/articles/view/2231664737)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `isActive` | body | `string` | no | Optional. Yes or No, selects only active projects. |
| `portfolio` | body | `string` | no | Optional. Code or name of the portfolio. |
