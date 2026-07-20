# List Workspaces with Grist

Finds workspaces in a Grist organization.

## Endpoint

- **Method:** `GET`
- **Path:** `/orgs/:orgId/workspaces`
- **Base URL:** `https://docs.getgrist.com/api`
- **Official documentation:** [List Workspaces](https://support.getgrist.com/api/#tag/workspaces/operation/listWorkspaces)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `orgId` | path | `list<number>` | yes | Organization ID or current |
