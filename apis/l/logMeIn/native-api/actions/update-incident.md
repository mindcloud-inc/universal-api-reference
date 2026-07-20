# Update Incident with LogMeIn

Updates an existing incident in LogMeIn.

## Endpoint

- **Method:** `PUT`
- **Path:** `/goto-resolve-ticketing/v1/incidents/:referenceNum`
- **Base URL:** `https://api.goto.com`
- **Official documentation:** [Update Incident](https://developer.goto.com/LogMeInResolve/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `referenceNum` | path | `string` | yes | Required incident reference number. |
| `title` | body | `string` | no | Updated incident title. |
| `summary` | body | `string` | no | Updated incident summary. |
| `assignedUserId` | body | `string` | no | Updated assigned user ID. |
| `priorityId` | body | `string` | no | Updated priority ID. |
| `dueDate` | body | `date` | no | Updated due date/time. |
| `tenant.uuid` | body | `string` | no | Tenant UUID. |
| `tagIdsToAdd[]` | body | `array<string>` | no | Tag IDs to add to the incident. |
