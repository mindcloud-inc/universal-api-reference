# Create reCAPTCHA V3 Task Proxyless with 2Captcha

Creates a proxyless reCAPTCHA v3 task in 2Captcha.

## Endpoint

- **Method:** `POST`
- **Path:** `/createTask`
- **Base URL:** `https://api.2captcha.com`
- **Official documentation:** [Create reCAPTCHA V3 Task Proxyless](https://2captcha.com/api-docs/recaptcha-v3)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `task.websiteURL` | body | `string` | yes |
| `task.websiteKey` | body | `string` | yes |
| `task.minScore` | body | `number` | yes |
| `task.pageAction` | body | `string` | no |
| `task.isEnterprise` | body | `boolean` | no |
| `task.apiDomain` | body | `string` | no |
