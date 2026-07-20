# Create Project Activity with Timewax

Creates a new project activity in Timewax.

## Endpoint

- **Method:** `POST`
- **Path:** `project/breakdown/add/`
- **Base URL:** `https://api.timewax.com/`
- **Official documentation:** [Create Project Activity](https://timewax.atlassian.net/rest/servicedesk/knowledgebase/latest/articles/view/2231631983)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `request.project` | body | `string` | yes | Code or name of the project. |
| `request.code` | body | `string` | yes | Code of the activity. |
| `request.name` | body | `string` | yes | Name of the activity. |
