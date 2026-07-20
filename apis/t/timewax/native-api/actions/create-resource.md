# Create Resource with Timewax

Creates a new resource in Timewax.

## Endpoint

- **Method:** `POST`
- **Path:** `resource/add/`
- **Base URL:** `https://api.timewax.com/`
- **Official documentation:** [Create Resource](https://timewax.atlassian.net/rest/servicedesk/knowledgebase/latest/articles/view/2231566461)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `request.code` | body | `string` | yes | Code of the resource. |
| `request.lastName` | body | `string` | yes | Last name of the resource. |
| `request.firstNames` | body | `string` | yes | First name(s) of the resource. |
| `request.organisationalUnit` | body | `string` | yes | Code or name of the department. |
| `request.position` | body | `string` | yes | Code or name of the position. |
| `request.startDate` | body | `date` | yes | Start date for the resource. |
