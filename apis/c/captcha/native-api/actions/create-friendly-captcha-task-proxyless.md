# Create Friendly Captcha Task Proxyless with 2Captcha

Creates a proxyless Friendly Captcha task in 2Captcha.

## Endpoint

- **Method:** `POST`
- **Path:** `/createTask`
- **Base URL:** `https://api.2captcha.com`
- **Official documentation:** [Create Friendly Captcha Task Proxyless](https://2captcha.com/api-docs/friendly-captcha)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `task.websiteURL` | body | `string` | yes |
| `task.websiteKey` | body | `string` | yes |
| `task.version` | body | `string` | no |
| `task.moduleScript` | body | `string` | no |
| `task.nomoduleScript` | body | `string` | no |
