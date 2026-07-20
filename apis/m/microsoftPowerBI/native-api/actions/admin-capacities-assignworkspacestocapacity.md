# Capacities AssignWorkspacesToCapacity with Microsoft Power BI

## Endpoint

- **Method:** `POST`
- **Path:** `admin/capacities/AssignWorkspaces`
- **Base URL:** `https://api.powerbi.com/v1.0/myorg`
- **Official documentation:** [Capacities AssignWorkspacesToCapacity](https://learn.microsoft.com/en-us/rest/api/power-bi/admin/capacities-assign-workspaces-to-capacity)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `capacityMigrationAssignments[]` | body | `array<object>` | no | Assignment contract for migrating workspaces to a premium capacity as tenant admin |
