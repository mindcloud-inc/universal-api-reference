# Create Arkose FunCaptcha Task Proxyless with 2Captcha

Creates a proxyless Arkose FunCaptcha task in 2Captcha.

## Endpoint

- **Method:** `POST`
- **Path:** `/createTask`
- **Base URL:** `https://api.2captcha.com`
- **Official documentation:** [Create Arkose FunCaptcha Task Proxyless](https://2captcha.com/api-docs/arkoselabs-funcaptcha)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `task.websiteURL` | body | `string` | yes |
| `task.websitePublicKey` | body | `string` | yes |
| `task.funcaptchaApiJSSubdomain` | body | `string` | no |
| `task.data` | body | `string` | no |
| `task.userAgent` | body | `string` | no |
