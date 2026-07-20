# Get Tasks with ServiceTitan

## Endpoint

- **Method:** `GET`
- **Path:** `taskmanagement/v2/tenant/{tenant}/tasks`
- **Base URL:** `https://{baseUrl}/`
- **Official documentation:** [Get Tasks](https://developer.servicetitan.io/api-details/#api=tenant-task-management-v2&operation=Tasks_GetTasks)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | query | `string` | no | — |
| `projectId` | query | `string` | no | — |
| `ids` | query | `string` | no | — |
| `statuses` | query | `string` | no | — |
| `active` | query | `string` | no | — |
| `customerId` | query | `string` | no | — |
| `includeSubtacks` | query | `boolean` | no | Format: `toggle`. |
| `jobId` | query | `string` | no | — |
| `createdOnOrAfter` | query | `string` | no | — |
| `modifiedOnOrAfter` | query | `string` | no | — |
| `employeeTaskResolutionIds` | query | `string` | no | — |
| `taskNumber` | query | `string` | no | — |
| `createdBefore` | query | `string` | no | — |
| `modifiedBefore` | query | `string` | no | — |
| `reportedBefore` | query | `string` | no | — |
| `reportedOnOrAfter` | query | `string` | no | — |
| `businessUnitIds` | query | `string` | no | — |
| `jobNumber` | query | `string` | no | — |
| `sort` | query | `string` | no | Applies sorting by the specified field: "?sort=+FieldName" for ascending order, "?sort=-FieldName" for descending order.  Available fields are: Id, CreatedOn, DescriptionModifiedOn, CompletedBy, Priority |
