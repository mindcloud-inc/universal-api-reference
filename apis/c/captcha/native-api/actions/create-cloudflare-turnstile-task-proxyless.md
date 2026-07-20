# Create Cloudflare Turnstile Task Proxyless with 2Captcha

Creates a proxyless Cloudflare Turnstile task in 2Captcha.

## Endpoint

- **Method:** `POST`
- **Path:** `/createTask`
- **Base URL:** `https://api.2captcha.com`
- **Official documentation:** [Create Cloudflare Turnstile Task Proxyless](https://2captcha.com/api-docs/cloudflare-turnstile)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `task.websiteURL` | body | `string` | yes |
| `task.websiteKey` | body | `string` | yes |
| `task.action` | body | `string` | no |
| `task.data` | body | `string` | no |
| `task.pagedata` | body | `string` | no |
