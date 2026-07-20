# Get Agent Performance Report with NeetoDesk

## Endpoint

- **Method:** `GET`
- **Path:** `/reports/agents`
- **Base URL:** `https://{workspaceSubdomain}.neetodesk.com/api/external/v2`
- **Official documentation:** [Get Agent Performance Report](https://apidocs.neetodesk.com/api-reference/reports/get-agent-performance)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `page_number` | query | `number` | no | Page number for the report results. |
| `range_type` | query | `string` | no | Date range preset for the report. |
| `start_date` | query | `date` | no | Start date for a custom range. |
| `end_date` | query | `date` | no | End date for a custom range. |
