# List Time Entries with Timewax

Retrieves time entry records from Timewax.

## Endpoint

- **Method:** `POST`
- **Path:** `time/entries/list/`
- **Base URL:** `https://api.timewax.com/`
- **Official documentation:** [List Time Entries](https://timewax.atlassian.net/rest/servicedesk/knowledgebase/latest/articles/view/2231566586)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `dateFrom` | body | `date` | yes | Required. Date from, format yyyymmdd or yyyy-mm-dd. |
| `dateTo` | body | `date` | yes | Required. Date to, format yyyymmdd or yyyy-mm-dd. |
