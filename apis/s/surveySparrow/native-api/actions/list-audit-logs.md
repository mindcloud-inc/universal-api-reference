# List Audit Logs with SurveySparrow

Retrieves audit logs from SurveySparrow.

## Endpoint

- **Method:** `GET`
- **Path:** `/audit_logs`
- **Base URL:** `https://api.surveysparrow.com/v3`
- **Official documentation:** [List Audit Logs](https://developers.surveysparrow.com/rest-apis/get-v-3-audit-logs/)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `event_type` | query | `list` | no | Type of audit log event |
| `start_date` | query | `date` | no | Start date of data range |
| `end_date` | query | `date` | no | End date of data range |
