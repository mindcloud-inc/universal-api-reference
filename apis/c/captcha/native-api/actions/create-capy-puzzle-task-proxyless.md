# Create Capy Puzzle Task Proxyless with 2Captcha

Creates a proxyless Capy Puzzle task in 2Captcha.

## Endpoint

- **Method:** `POST`
- **Path:** `/createTask`
- **Base URL:** `https://api.2captcha.com`
- **Official documentation:** [Create Capy Puzzle Task Proxyless](https://2captcha.com/api-docs/capy-puzzle-captcha)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `task.websiteURL` | body | `string` | yes |
| `task.websiteKey` | body | `string` | yes |
| `task.userAgent` | body | `string` | no |
