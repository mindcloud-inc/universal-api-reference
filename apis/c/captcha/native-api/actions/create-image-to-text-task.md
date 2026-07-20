# Create Image To Text Task with 2Captcha

Creates an image-to-text captcha task in 2Captcha.

## Endpoint

- **Method:** `POST`
- **Path:** `/createTask`
- **Base URL:** `https://api.2captcha.com`
- **Official documentation:** [Create Image To Text Task](https://2captcha.com/api-docs/normal-captcha)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `task.body` | body | `string` | yes |
| `task.phrase` | body | `boolean` | no |
| `task.case` | body | `boolean` | no |
| `task.numeric` | body | `number` | no |
| `task.math` | body | `boolean` | no |
| `task.minLength` | body | `number` | no |
| `task.maxLength` | body | `number` | no |
| `task.comment` | body | `string` | no |
| `task.imgInstructions` | body | `string` | no |
