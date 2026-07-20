# Create Amazon WAF Task Proxyless with 2Captcha

Creates a proxyless Amazon WAF captcha task in 2Captcha.

## Endpoint

- **Method:** `POST`
- **Path:** `/createTask`
- **Base URL:** `https://api.2captcha.com`
- **Official documentation:** [Create Amazon WAF Task Proxyless](https://2captcha.com/api-docs/amazon-aws-waf-captcha)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `task.websiteURL` | body | `string` | yes |
| `task.websiteKey` | body | `string` | yes |
| `task.iv` | body | `string` | yes |
| `task.context` | body | `string` | yes |
| `task.challengeScript` | body | `string` | no |
| `task.captchaScript` | body | `string` | no |
