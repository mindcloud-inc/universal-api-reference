# Save echeck token with Nexiopay

## Endpoint

- **Method:** `POST`
- **Path:** `/pay/v3/saveECheck`
- **Base URL:** `https://api.nexiopaysandbox.com`
- **Official documentation:** [Save echeck token](https://docs.nexiopay.com/reference/saveechecktoken)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `token` | body | `string` | yes | One-time-use token returned by the token endpoint. |
| `bank` | body | `object` | yes | Bank account information object documented by Nexio. |
