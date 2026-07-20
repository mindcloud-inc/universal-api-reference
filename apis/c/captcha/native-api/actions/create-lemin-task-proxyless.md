# Create Lemin Task Proxyless with 2Captcha

Creates a proxyless Lemin captcha task in 2Captcha.

## Endpoint

- **Method:** `POST`
- **Path:** `/createTask`
- **Base URL:** `https://api.2captcha.com`
- **Official documentation:** [Create Lemin Task Proxyless](https://2captcha.com/api-docs/lemin)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `task.websiteURL` | body | `string` | yes |
| `task.captchaId` | body | `string` | yes |
| `task.divId` | body | `string` | yes |
| `task.leminApiServerSubdomain` | body | `string` | no |
| `task.userAgent` | body | `string` | no |
