# List Planning Bookings with Timewax

Retrieves planning booking records from Timewax.

## Endpoint

- **Method:** `POST`
- **Path:** `calendar/entries/list/`
- **Base URL:** `https://api.timewax.com/`
- **Official documentation:** [List Planning Bookings](https://timewax.atlassian.net/rest/servicedesk/knowledgebase/latest/articles/view/2231664838)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `dateFrom` | body | `date` | yes | Required. Date from, format yyyymmdd or yyyy-mm-dd. |
| `dateTo` | body | `date` | yes | Required. Date to, format yyyymmdd or yyyy-mm-dd. |
