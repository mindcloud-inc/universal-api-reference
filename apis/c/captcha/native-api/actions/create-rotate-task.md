# Create Rotate Task with 2Captcha

Creates a rotate captcha task in 2Captcha.

## Endpoint

- **Method:** `POST`
- **Path:** `/createTask`
- **Base URL:** `https://api.2captcha.com`
- **Official documentation:** [Create Rotate Task](https://2captcha.com/api-docs/rotate)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `task.body` | body | `string` | yes |
| `task.angle` | body | `number` | no |
| `task.comment` | body | `string` | no |
| `task.imgInstructions` | body | `string` | no |
