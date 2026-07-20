# Create Client with Timewax

Creates a new client in Timewax.

## Endpoint

- **Method:** `POST`
- **Path:** `company/add/`
- **Base URL:** `https://api.timewax.com/`
- **Official documentation:** [Create Client](https://timewax.atlassian.net/rest/servicedesk/knowledgebase/latest/articles/view/2230878315)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `code` | body | `string` | yes | Required. Code of the client. |
| `name` | body | `string` | yes | Required. Name of the client. |
