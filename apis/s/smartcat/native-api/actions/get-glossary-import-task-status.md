# Get Glossary Import Task Status with Smartcat

Retrieves glossary import task status from Smartcat.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/integration/v1/glossary/importTaskState/:taskId`
- **Base URL:** `https://smartcat.ai`
- **Official documentation:** [Get Glossary Import Task Status](https://developers.smartcat.com/api/#fetch-the-status-of-a-concept-import-task)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `taskId` | path | `string` | yes | Smartcat glossary import task ID |
