# Report Incorrect with 2Captcha

Marks a 2Captcha task result as incorrect.

## Endpoint

- **Method:** `POST`
- **Path:** `/reportIncorrect`
- **Base URL:** `https://api.2captcha.com`
- **Official documentation:** [Report Incorrect](https://2captcha.com/api-docs/report-incorrect)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `taskId` | body | `number` | yes | Task id to report as incorrectly solved. |
