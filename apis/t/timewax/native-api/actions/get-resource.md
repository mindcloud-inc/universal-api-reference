# Get Resource with Timewax

Retrieves a resource from Timewax.

## Endpoint

- **Method:** `POST`
- **Path:** `resource/get/`
- **Base URL:** `https://api.timewax.com/`
- **Official documentation:** [Get Resource](https://timewax.atlassian.net/rest/servicedesk/knowledgebase/latest/articles/view/2231664819)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `resource` | body | `string` | yes | Required. Name, full name, or email of the resource. |
