# Create Project with TMetric

## Endpoint

- **Method:** `POST`
- **Path:** `/accounts/:accountId/projects`
- **Base URL:** `https://app.tmetric.com/api/v3`
- **Official documentation:** [Create Project](https://app.tmetric.com/api-docs/#/Projects/post-accounts-accountId-projects)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `accountId` | path | `number` | yes | Workspace identifier. |
| `client.id` | body | `number` | no | Client identifier. |
| `invoiceMethod` | body | `string` | no | Invoice method for the project. |
| `isBillable` | body | `boolean` | no | Whether the project is billable. |
| `name` | body | `string` | no | Project name. |
| `status` | body | `string` | no | Project status. |
