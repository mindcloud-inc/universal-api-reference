# Generate User Session Key with Pastebin

Creates a Pastebin user session key.

## Endpoint

- **Method:** `POST`
- **Path:** `/api_login.php`
- **Base URL:** `https://pastebin.com/api`
- **Official documentation:** [Generate User Session Key](https://pastebin.com/doc_api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `api_user_name` | body | `string` | yes | Pastebin username used to generate an api_user_key. |
| `api_user_password` | body | `string` | yes | Pastebin password used to generate an api_user_key. |
