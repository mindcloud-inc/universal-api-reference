# Create Account with ChatDaddy

Creates a new account in ChatDaddy.

## Endpoint

- **Method:** `POST`
- **Path:** `/accounts`
- **Base URL:** `https://api.chatdaddy.tech/im`
- **Official documentation:** [Create Account](https://chatdaddy.stoplight.io/docs/openapi/ae125c4f23616-add-a-new-account)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `type` | body | `string` | yes | Account channel type. Verified live values include `wa`, `messenger`, and `instagram`. |
