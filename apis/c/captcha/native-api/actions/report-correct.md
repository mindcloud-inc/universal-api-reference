# Report Correct with 2Captcha

Marks a 2Captcha task result as correct.

## Endpoint

- **Method:** `POST`
- **Path:** `/reportCorrect`
- **Base URL:** `https://api.2captcha.com`
- **Official documentation:** [Report Correct](https://2captcha.com/api-docs/report-correct)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `taskId` | body | `number` | yes | Task id to report as correctly solved. |
