# Create Secret with Password.link

## Endpoint

- **Method:** `POST`
- **Path:** `/secrets`
- **Base URL:** `https://password.link/api`
- **Official documentation:** [Create Secret](https://password.link/en/p/docs/api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `ciphertext` | body | `string` | yes | SJCL-compatible Base64 ciphertext for the secret. |
| `password_part_private` | body | `string` | yes | Private password part in Base64. |
| `description` | body | `string` | no | Optional secret description. |
| `message` | body | `string` | no | Optional message shown with the secret. |
| `expiration` | body | `number` | no | Expiration time in hours. |
| `view_button` | body | `boolean` | no | Show a view secret button instead of showing the secret immediately. |
| `captcha` | body | `boolean` | no | Show a simple CAPTCHA before showing the secret. |
| `password` | body | `string` | no | Optional password required to view the secret. |
| `max_views` | body | `number` | no | Maximum number of times the secret can be viewed. Possible values are 1-100. |
