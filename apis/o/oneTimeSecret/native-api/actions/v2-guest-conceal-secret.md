# Guest Conceal Secret with One-Time Secret

Creates a guest secret from provided content in One-Time Secret.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v2/guest/secret/conceal`
- **Base URL:** `https://us.onetimesecret.com`
- **Official documentation:** [Guest Conceal Secret](https://api.onetimesecret.com/doc/api-v2/operation/operation-v2_guest_concealsecret)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `secret.share_domain` | body | `string` | yes | Domain used for generated share URLs. |
| `secret.secret` | body | `string` | yes | The secret text to conceal. |
