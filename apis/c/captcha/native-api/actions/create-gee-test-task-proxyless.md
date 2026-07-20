# Create GeeTest Task Proxyless with 2Captcha

Creates a proxyless GeeTest task in 2Captcha.

## Endpoint

- **Method:** `POST`
- **Path:** `/createTask`
- **Base URL:** `https://api.2captcha.com`
- **Official documentation:** [Create GeeTest Task Proxyless](https://2captcha.com/api-docs/geetest)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `task.websiteURL` | body | `string` | yes |
| `task.gt` | body | `string` | yes |
| `task.challenge` | body | `string` | yes |
| `task.geetestApiServerSubdomain` | body | `string` | no |
| `task.userAgent` | body | `string` | no |
| `task.version` | body | `number` | no |
| `task.initParameters` | body | `object` | no |
| `task.risk_type` | body | `string` | no |
