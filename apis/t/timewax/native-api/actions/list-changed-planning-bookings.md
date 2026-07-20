# List Changed Planning Bookings with Timewax

Retrieves changed planning bookings from Timewax by date range.

## Endpoint

- **Method:** `POST`
- **Path:** `calendar/entries/list_changed/`
- **Base URL:** `https://api.timewax.com/`
- **Official documentation:** [List Changed Planning Bookings](https://timewax.atlassian.net/rest/servicedesk/knowledgebase/latest/articles/view/2231566556)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `dateFrom` | body | `date` | yes | Required. Add or modification date from, format yyyymmdd or yyyy-mm-dd. |
| `dateTo` | body | `date` | yes | Required. Add or modification date to, format yyyymmdd or yyyy-mm-dd. |
