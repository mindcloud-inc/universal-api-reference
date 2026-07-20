# Get Ticket Status 24h Distribution Report with HelpDesk

Retrieves the 24-hour ticket status distribution from HelpDesk.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/reports/status24`
- **Base URL:** `https://api.helpdesk.com`
- **Official documentation:** [Get Ticket Status 24h Distribution Report](https://api.helpdesk.com/docs#tag/Reports/operation/reportStatus24)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `status` | query | `string` | yes | Ticket status for the 24h distribution report. |
