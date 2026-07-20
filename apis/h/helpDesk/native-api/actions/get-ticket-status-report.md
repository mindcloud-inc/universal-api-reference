# Get Ticket Status Report with HelpDesk

Retrieves the ticket status report from HelpDesk.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/reports/status`
- **Base URL:** `https://api.helpdesk.com`
- **Official documentation:** [Get Ticket Status Report](https://api.helpdesk.com/docs#tag/Reports/operation/reportStatus)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `status` | query | `string` | yes | Ticket status for the report. |
