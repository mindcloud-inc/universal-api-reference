# Capacities UnassignWorkspacesFromCapacity with Microsoft Power BI

## Endpoint

- **Method:** `POST`
- **Path:** `admin/capacities/UnassignWorkspaces`
- **Base URL:** `https://api.powerbi.com/v1.0/myorg`
- **Official documentation:** [Capacities UnassignWorkspacesFromCapacity](https://learn.microsoft.com/en-us/rest/api/power-bi/admin/capacities-unassign-workspaces-from-capacity)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `workspacesToUnassign[]` | body | `array<string>` | yes | The workspaces to migrate to a shared capacity |
