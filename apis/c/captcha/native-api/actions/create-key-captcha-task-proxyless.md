# Create KeyCaptcha Task Proxyless with 2Captcha

Creates a proxyless KeyCaptcha task in 2Captcha.

## Endpoint

- **Method:** `POST`
- **Path:** `/createTask`
- **Base URL:** `https://api.2captcha.com`
- **Official documentation:** [Create KeyCaptcha Task Proxyless](https://2captcha.com/api-docs/keycaptcha)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `task.websiteURL` | body | `string` | yes |
| `task.s_s_c_user_id` | body | `string` | yes |
| `task.s_s_c_session_id` | body | `string` | yes |
| `task.s_s_c_web_server_sign` | body | `string` | yes |
| `task.s_s_c_web_server_sign2` | body | `string` | yes |
