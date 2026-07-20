# Create Incident with LogMeIn

Creates a new incident in LogMeIn.

## Endpoint

- **Method:** `POST`
- **Path:** `/goto-resolve-ticketing/v1/incidents`
- **Base URL:** `https://api.goto.com`
- **Official documentation:** [Create Incident](https://developer.goto.com/LogMeInResolve/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `title` | body | `string` | yes | Incident title. |
| `serviceId` | body | `string` | yes | Service identifier for the incident. |
| `priorityId` | body | `string` | no | Priority identifier. |
| `summary` | body | `string` | yes | Incident summary. |
| `dueDate` | body | `date` | no | Incident due date/time. |
| `tenantUuid` | body | `string` | no | Tenant UUID for the incident. |
| `assignedUserId` | body | `string` | no | Assigned user ID. |
| `categoryId` | body | `string` | no | Category ID. |
| `tagIds[]` | body | `array<string>` | no | Tag IDs to attach to the incident. |
