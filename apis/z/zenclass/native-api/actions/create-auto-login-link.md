# Create auto login link with Zenclass

Creates a one-click login link in Zenclass.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/auto_login_link`
- **Base URL:** `https://api.zenclass.net`
- **Official documentation:** [Create auto login link](https://docs.zenclass.ru)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `data.redirect_path` | body | `string` | yes | School-relative path to open after sign-in. |
| `email` | body | `string` | yes | Student email address. |
