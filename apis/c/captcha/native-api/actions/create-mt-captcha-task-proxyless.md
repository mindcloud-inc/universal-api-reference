# Create MTCaptcha Task Proxyless with 2Captcha

Creates a proxyless MTCaptcha task in 2Captcha.

## Endpoint

- **Method:** `POST`
- **Path:** `/createTask`
- **Base URL:** `https://api.2captcha.com`
- **Official documentation:** [Create MTCaptcha Task Proxyless](https://2captcha.com/api-docs/mtcaptcha)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `task.websiteURL` | body | `string` | yes |
| `task.websiteKey` | body | `string` | yes |
