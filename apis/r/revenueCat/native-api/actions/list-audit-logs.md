# List Audit Logs with RevenueCat

Retrieves audit logs from RevenueCat.

## Endpoint

- **Method:** `GET`
- **Path:** `projects/:projectId/audit_logs`
- **Base URL:** `https://api.revenuecat.com/v2`
- **Official documentation:** [List Audit Logs](https://www.revenuecat.com/docs/api-v2#tag/Audit-Log)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `projectId` | path | `string` | yes | RevenueCat project ID. Defaults to the project associated with the configured credential. |
