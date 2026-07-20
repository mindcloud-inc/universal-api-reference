# List My Shared Reports with Clockify

Lists your shared reports in Clockify.

## Endpoint

- **Method:** `GET`
- **Path:** `workspaces/:workspaceId/shared-reports`
- **Base URL:** `https://api.clockify.me/api/v1`
- **Official documentation:** [List My Shared Reports](https://docs.developer.clockify.me/#tag/Shared-Report/operation/getSharedReportsV1)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `page` | query | `number` | no | — |
| `pageSize` | query | `number` | no | — |
| `sharedReportsFilter` | query | `list` | no | Accepted values: `ALL`, `CREATED_BY_ME`, `SHARED_WITH_ME`. |
| `workspaceId` | path | `list<string>` | yes | — |
