# Get Folder Surveys with QuestionPro Surveys

## Endpoint

- **Method:** `GET`
- **Path:** `users/:userId/folders/:folderId/surveys`
- **Base URL:** `https://api.questionpro.com/a/api/v2`
- **Official documentation:** [Get Folder Surveys](https://www.questionpro.com/api/get-folder-surveys.html)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `userId` | path | `number` | yes | The QuestionPro user ID. |
| `folderId` | path | `number` | yes | The QuestionPro folder ID. |
