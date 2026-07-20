# Get Task Result with 2Captcha

Retrieves the current result for a 2Captcha task.

## Endpoint

- **Method:** `POST`
- **Path:** `/getTaskResult`
- **Base URL:** `https://api.2captcha.com`
- **Official documentation:** [Get Task Result](https://2captcha.com/api-docs/get-task-result)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `taskId` | body | `number` | yes | 2Captcha task id returned by createTask. |
