# List Changed Projects with Timewax

Retrieves changed projects from Timewax by date range.

## Endpoint

- **Method:** `POST`
- **Path:** `project/list_changed/`
- **Base URL:** `https://api.timewax.com/`
- **Official documentation:** [List Changed Projects](https://timewax.atlassian.net/rest/servicedesk/knowledgebase/latest/articles/view/2231664714)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `dateFrom` | body | `date` | yes | Required. Add or modification date from, format yyyymmdd or yyyy-mm-dd. |
| `dateTo` | body | `date` | yes | Required. Add or modification date to, format yyyymmdd or yyyy-mm-dd. |
