# Create Task with ServiceTitan

## Endpoint

- **Method:** `POST`
- **Path:** `taskmanagement/v2/tenant/{tenant}/tasks`
- **Base URL:** `https://{baseUrl}/`
- **Official documentation:** [Create Task](https://developer.servicetitan.io/api-details/#api=tenant-task-management-v2&operation=Tasks_Create)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | body | `string` | yes | — |
| `projectId` | body | `number` | no | — |
| `jobId` | body | `number` | no | — |
| `customerId` | body | `number` | no | Format: `toggle`. |
| `description` | body | `string` | no | — |
| `reportedById` | body | `number` | yes | — |
| `assignedToId` | body | `number` | yes | — |
| `isClosed` | body | `boolean` | yes | Format: `toggle`. |
| `businessUnitId` | body | `number` | yes | — |
| `employeeTaskTypeId` | body | `string` | yes | — |
| `employeeTaskSourceId` | body | `string` | yes | — |
| `reportedDate` | body | `date` | yes | — |
| `priority` | body | `string` | yes | — |
| `employeeTaskResolutionId` | body | `number` | no | — |
| `completeBy` | body | `date` | no | — |
| `startedOn` | body | `date` | no | — |
| `involvedEmployeeIdList[]` | body | `array` | no | — |
| `status` | body | `string` | no | — |
