# Create Position with Timewax

Creates a new position in Timewax.

## Endpoint

- **Method:** `POST`
- **Path:** `position/add/`
- **Base URL:** `https://api.timewax.com/`
- **Official documentation:** [Create Position](https://timewax.atlassian.net/rest/servicedesk/knowledgebase/latest/articles/view/2231468168)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `code` | body | `string` | yes | Required. Code of the position. |
| `name` | body | `string` | yes | Required. Name of the position. |
