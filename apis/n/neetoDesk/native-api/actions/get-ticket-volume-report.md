# Get Ticket Volume Report with NeetoDesk

## Endpoint

- **Method:** `GET`
- **Path:** `/reports/tickets`
- **Base URL:** `https://{workspaceSubdomain}.neetodesk.com/api/external/v2`
- **Official documentation:** [Get Ticket Volume Report](https://apidocs.neetodesk.com/api-reference/reports/get-ticket-volume)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `range_type` | query | `string` | no | Date range preset for the report. |
| `start_date` | query | `date` | no | Start date for a custom range. |
| `end_date` | query | `date` | no | End date for a custom range. |
