# Update Position with Timewax

Updates an existing position in Timewax.

## Endpoint

- **Method:** `POST`
- **Path:** `position/edit/`
- **Base URL:** `https://api.timewax.com/`
- **Official documentation:** [Update Position](https://timewax.atlassian.net/rest/servicedesk/knowledgebase/latest/articles/view/2259681281)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `position` | body | `string` | yes | Required. Code or name of the position to edit. |
| `code` | body | `string` | yes | Required. New code of the position. |
| `name` | body | `string` | yes | Required. New name of the position. |
