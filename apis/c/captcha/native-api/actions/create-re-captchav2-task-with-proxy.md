# Create reCAPTCHA V2 Task With Proxy with 2Captcha

Creates a proxied reCAPTCHA v2 task in 2Captcha.

## Endpoint

- **Method:** `POST`
- **Path:** `/createTask`
- **Base URL:** `https://api.2captcha.com`
- **Official documentation:** [Create reCAPTCHA V2 Task With Proxy](https://2captcha.com/api-docs/recaptcha-v2)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `task.websiteURL` | body | `string` | yes | — |
| `task.websiteKey` | body | `string` | yes | — |
| `task.recaptchaDataSValue` | body | `string` | no | — |
| `task.isInvisible` | body | `boolean` | no | — |
| `task.userAgent` | body | `string` | no | — |
| `task.cookies` | body | `string` | no | — |
| `task.apiDomain` | body | `string` | no | — |
| `task.proxyType` | body | `string` | yes | Proxy type: http, socks4, or socks5. |
| `task.proxyAddress` | body | `string` | yes | Proxy IP address or hostname. |
| `task.proxyPort` | body | `number` | yes | Proxy port. |
| `task.proxyLogin` | body | `string` | no | Proxy login for basic authentication. |
| `task.proxyPassword` | body | `string` | no | Proxy password for basic authentication. |
