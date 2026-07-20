# Save card token with Nexiopay

## Endpoint

- **Method:** `POST`
- **Path:** `/pay/v3/saveCard`
- **Base URL:** `https://api.nexiopaysandbox.com`
- **Official documentation:** [Save card token](https://docs.nexiopay.com/reference/savecardtoken)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `token` | body | `string` | yes | One-time-use token returned by the token endpoint. |
| `card` | body | `object` | yes | Card information object documented by Nexio. |
