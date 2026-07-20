# List In-Progress Time Entries with Clockify

Lists in-progress time entries in Clockify.

## Endpoint

- **Method:** `GET`
- **Path:** `workspaces/:workspaceId/time-entries/status/in-progress`
- **Base URL:** `https://api.clockify.me/api/v1`
- **Official documentation:** [List In-Progress Time Entries](https://docs.developer.clockify.me/#tag/Time-entry/operation/getInProgressTimeEntries)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `workspaceId` | path | `list<string>` | yes |
