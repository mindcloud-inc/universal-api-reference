# Get Tickets Status Per Team Report with HelpDesk

Retrieves the ticket status per team report from HelpDesk.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/reports/statusPerTeam`
- **Base URL:** `https://api.helpdesk.com`
- **Official documentation:** [Get Tickets Status Per Team Report](https://api.helpdesk.com/docs#tag/Reports/operation/reportStatusPerTeam)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `status` | query | `string` | yes | Ticket status for the report. |
