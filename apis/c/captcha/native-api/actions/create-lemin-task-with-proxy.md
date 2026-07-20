# Create Lemin Task With Proxy with 2Captcha

Creates a proxied Lemin captcha task in 2Captcha.

## Endpoint

- **Method:** `POST`
- **Path:** `/createTask`
- **Base URL:** `https://api.2captcha.com`
- **Official documentation:** [Create Lemin Task With Proxy](https://2captcha.com/api-docs/lemin)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `task.websiteURL` | body | `string` | yes | — |
| `task.captchaId` | body | `string` | yes | — |
| `task.divId` | body | `string` | yes | — |
| `task.leminApiServerSubdomain` | body | `string` | no | — |
| `task.userAgent` | body | `string` | no | — |
| `task.proxyType` | body | `string` | yes | Proxy type: http, socks4, or socks5. |
| `task.proxyAddress` | body | `string` | yes | Proxy IP address or hostname. |
| `task.proxyPort` | body | `number` | yes | Proxy port. |
| `task.proxyLogin` | body | `string` | no | Proxy login for basic authentication. |
| `task.proxyPassword` | body | `string` | no | Proxy password for basic authentication. |
