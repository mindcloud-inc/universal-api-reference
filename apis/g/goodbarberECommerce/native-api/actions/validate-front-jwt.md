# Validate Front JWT with Goodbarber eCommerce

## Endpoint

- **Method:** `POST`
- **Path:** `/publicapi/v2/general/customer/:webzine_id/auth/validate/`
- **Base URL:** `https://commerce.goodbarber.dev`
- **Official documentation:** [Validate Front JWT](https://commerce.goodbarber.dev/publicapi/v2/documentation/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `user_id` | body | `string` | yes | Unique ID of the user against which the token should be validated. |
| `jwt` | body | `string` | yes | Token to validate. |
