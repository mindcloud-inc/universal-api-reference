# List Audit Log Events with SurveySparrow

Retrieves subscribed audit log events from SurveySparrow.

## Endpoint

- **Method:** `GET`
- **Path:** `/audit_logs/events`
- **Base URL:** `https://api.surveysparrow.com/v3`
- **Official documentation:** [List Audit Log Events](https://developers.surveysparrow.com/rest-apis/get-v-3-audit-logs-events/)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `event_type` | query | `list` | no | Type of the event |
