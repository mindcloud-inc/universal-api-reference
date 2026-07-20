# Register Sub User with Ship&Co

## Endpoint

- **Method:** `POST`
- **Path:** `/sub-users`
- **Base URL:** `https://api.shipandco.com/v1`
- **Official documentation:** [Register Sub User](https://developer.shipandco.com/en/#sub-user)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `email` | body | `string` | yes | Sub-user email address. |
| `api_token` | body | `boolean` | no | Whether Ship&Co should generate an API token for the sub-user. |
| `contact` | body | `object` | no | Sub-user contact object. |
