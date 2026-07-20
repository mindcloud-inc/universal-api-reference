# Calculate Single Simple with SpreadsheetWeb Hub

Performs a simplified single calculation in SpreadsheetWeb Hub.

## Endpoint

- **Method:** `POST`
- **Path:** `/calculations/calculatesinglesimple`
- **Base URL:** `https://api.spreadsheetweb.com`
- **Official documentation:** [Calculate Single Simple](https://api.spreadsheetweb.com/index.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `request` | body | `object` | no | Primary request payload. |
| `request.applicationId` | body | `string` | yes | SpreadsheetWeb application UUID. |
| `request.workspaceId` | body | `string` | yes | SpreadsheetWeb workspace UUID. |
| `request.inputs` | body | `object` | no | Input values keyed by named range. |
| `request.outputs[]` | body | `array<string>` | no | Named outputs to return. |
