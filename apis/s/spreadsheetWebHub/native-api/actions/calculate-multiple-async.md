# Calculate Multiple Async with SpreadsheetWeb Hub

Performs multiple asynchronous calculations in SpreadsheetWeb Hub.

## Endpoint

- **Method:** `POST`
- **Path:** `/calculations/calculatemultipleasync`
- **Base URL:** `https://api.spreadsheetweb.com`
- **Official documentation:** [Calculate Multiple Async](https://api.spreadsheetweb.com/index.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `request.applicationId` | body | `string` | yes | SpreadsheetWeb application identifier for the async bulk calculation request. |
| `request.workspaceId` | body | `string` | yes | Workspace identifier for the async bulk calculation request. |
| `request.inputs` | body | `object` | no | Dictionary of calculation inputs keyed by request item identifier. |
