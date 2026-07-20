# Create Tencent Captcha Task Proxyless with 2Captcha

Creates a proxyless Tencent captcha task in 2Captcha.

## Endpoint

- **Method:** `POST`
- **Path:** `/createTask`
- **Base URL:** `https://api.2captcha.com`
- **Official documentation:** [Create Tencent Captcha Task Proxyless](https://2captcha.com/api-docs/tencent)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `task.websiteURL` | body | `string` | yes |
| `task.appId` | body | `string` | yes |
| `task.captchaScript` | body | `string` | no |
