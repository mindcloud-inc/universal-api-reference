# Create reCAPTCHA V2 Enterprise Task Proxyless with 2Captcha

Creates a proxyless reCAPTCHA v2 Enterprise task in 2Captcha.

## Endpoint

- **Method:** `POST`
- **Path:** `/createTask`
- **Base URL:** `https://api.2captcha.com`
- **Official documentation:** [Create reCAPTCHA V2 Enterprise Task Proxyless](https://2captcha.com/api-docs/recaptcha-v2-enterprise)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `task.websiteURL` | body | `string` | yes |
| `task.websiteKey` | body | `string` | yes |
| `task.enterprisePayload` | body | `object` | no |
| `task.isInvisible` | body | `boolean` | no |
| `task.userAgent` | body | `string` | no |
| `task.cookies` | body | `string` | no |
| `task.apiDomain` | body | `string` | no |
