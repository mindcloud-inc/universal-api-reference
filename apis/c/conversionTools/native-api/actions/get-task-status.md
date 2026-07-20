# Get Task Status with Conversion Tools

Retrieves the current status of a conversion task from Conversion Tools.

## Endpoint

- **Method:** `GET`
- **Path:** `/tasks/:taskId`
- **Base URL:** `https://api.conversiontools.io/v1`
- **Official documentation:** [Get Task Status](https://conversiontools.io/api-documentation#get-task-status)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `taskId` | path | `string` | yes | The task ID returned by task creation. |
