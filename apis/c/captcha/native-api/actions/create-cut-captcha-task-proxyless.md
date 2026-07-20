# Create CutCaptcha Task Proxyless with 2Captcha

Creates a proxyless CutCaptcha task in 2Captcha.

## Endpoint

- **Method:** `POST`
- **Path:** `/createTask`
- **Base URL:** `https://api.2captcha.com`
- **Official documentation:** [Create CutCaptcha Task Proxyless](https://2captcha.com/api-docs/cutcaptcha)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `task.websiteURL` | body | `string` | yes |
| `task.miseryKey` | body | `string` | yes |
| `task.apiKey` | body | `string` | yes |
