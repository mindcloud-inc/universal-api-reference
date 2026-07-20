# Audit Database with ActivityInfo

Retrieves audit entries for an ActivityInfo database.

## Endpoint

- **Method:** `POST`
- **Path:** `/resources/databases/:databaseId/audit`
- **Base URL:** `https://www.activityinfo.org`
- **Official documentation:** [Audit Database](https://www.activityinfo.org/support/docs/api/reference/auditDatabase.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `databaseId` | path | `string` | yes | ActivityInfo database ID. |
| `typeFilter[]` | body | `array<string>` | yes | Audit event resource types to include. |
| `startTime` | body | `number` | yes | Start time in milliseconds since epoch. |
