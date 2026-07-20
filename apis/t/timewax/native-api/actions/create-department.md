# Create Department with Timewax

Creates a new department in Timewax.

## Endpoint

- **Method:** `POST`
- **Path:** `department/add/`
- **Base URL:** `https://api.timewax.com/`
- **Official documentation:** [Create Department](https://timewax.atlassian.net/rest/servicedesk/knowledgebase/latest/articles/view/2230878382)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `code` | body | `string` | yes | Required. Code of the department. |
| `name` | body | `string` | yes | Required. Name of the department. |
| `manager` | body | `string` | yes | Required. Code or name of the resource that is the department manager. |
