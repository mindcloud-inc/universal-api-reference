# List Project Activities with Timewax

Retrieves all project activities from Timewax.

## Endpoint

- **Method:** `POST`
- **Path:** `project/breakdown/list/`
- **Base URL:** `https://api.timewax.com/`
- **Official documentation:** [List Project Activities](https://timewax.atlassian.net/rest/servicedesk/knowledgebase/latest/articles/view/2231566408)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `project` | body | `string` | yes | Required. Code or name of the project. |
