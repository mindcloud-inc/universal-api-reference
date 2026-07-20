# List Feature Audit Entries with DevCycle

Retrieves audit entries for a feature from DevCycle.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/projects/:project/features/:feature/audit`
- **Base URL:** `https://api.devcycle.com`
- **Official documentation:** [List Feature Audit Entries](https://docs.devcycle.com/management-api/#tag/Audit-Log/operation/AuditLogController_findAll)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `feature` | path | `string` | no | Feature key. |
| `project` | path | `string` | no | Project key. |
