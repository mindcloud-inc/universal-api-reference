# List Time Entries with NeetoInvoice

Retrieves unbilled time entries from NeetoInvoice.

## Endpoint

- **Method:** `GET`
- **Path:** `/time_entries`
- **Base URL:** `https://{workspaceSubdomain}.neetoinvoice.com/api/external/v1`
- **Official documentation:** [List Time Entries](https://apidocs.neetoinvoice.com/api-reference/time-entry/list)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `project_id` | query | `string` | no | Optional project filter for time entries. |
| `user_id` | query | `string` | no | Optional user filter for time entries. |
