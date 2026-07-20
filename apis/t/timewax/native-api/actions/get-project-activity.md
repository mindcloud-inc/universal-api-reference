# Get Project Activity with Timewax

Retrieves a project activity from Timewax.

## Endpoint

- **Method:** `POST`
- **Path:** `project/breakdown/get/`
- **Base URL:** `https://api.timewax.com/`
- **Official documentation:** [Get Project Activity](https://timewax.atlassian.net/rest/servicedesk/knowledgebase/latest/articles/view/2231664770)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `project` | body | `string` | yes | Required. Code or name of the project. |
| `breakdown` | body | `string` | yes | Required. Code or name of the activity. |
