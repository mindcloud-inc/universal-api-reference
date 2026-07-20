# Get Labeling Task with Clarifai

Retrieves a labeling task from Clarifai.

## Endpoint

- **Method:** `GET`
- **Path:** `/v2/users/{userId}/apps/{{appId}}/tasks/{{taskId}}`
- **Base URL:** `https://api.clarifai.com`
- **Official documentation:** [Get Labeling Task](https://docs.clarifai.com/create/labeling/api/tasks/)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `appId` | path | `string` | no |
| `taskId` | path | `string` | no |
