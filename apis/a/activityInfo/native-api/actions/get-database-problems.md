# Get Database Problems with ActivityInfo

Retrieves reported database problems from ActivityInfo.

## Endpoint

- **Method:** `POST`
- **Path:** `/resources/databases/:databaseId/problems`
- **Base URL:** `https://www.activityinfo.org`
- **Official documentation:** [Get Database Problems](https://www.activityinfo.org/support/docs/api/reference/getDatabaseProblems.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `databaseId` | path | `string` | yes | ActivityInfo database ID. |
| `typeFilter[]` | body | `array<string>` | yes | Problem types to include. |
| `statusFilter` | body | `string` | no | Problem status to include. |
