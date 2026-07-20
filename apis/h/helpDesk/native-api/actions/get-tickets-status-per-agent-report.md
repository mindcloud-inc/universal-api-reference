# Get Tickets Status Per Agent Report with HelpDesk

Retrieves the ticket status per agent report from HelpDesk.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/reports/statusPerAgent`
- **Base URL:** `https://api.helpdesk.com`
- **Official documentation:** [Get Tickets Status Per Agent Report](https://api.helpdesk.com/docs#tag/Reports/operation/reportStatusPerAgent)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `status` | query | `string` | yes | Ticket status for the report. |
