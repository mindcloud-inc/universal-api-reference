# Update Project Activity with Timewax

Updates an existing project activity in Timewax.

## Endpoint

- **Method:** `POST`
- **Path:** `project/breakdown/edit/`
- **Base URL:** `https://api.timewax.com/`
- **Official documentation:** [Update Project Activity](https://timewax.atlassian.net/rest/servicedesk/knowledgebase/latest/articles/view/2231566418)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `request.project` | body | `string` | yes | Code or name of the project. |
| `request.breakdown` | body | `string` | yes | Code or name of the activity. |
