# Create Lead with AdvantShop

Creates a new lead in AdvantShop.

## Endpoint

- **Method:** `POST`
- **Path:** `/leads/add`
- **Base URL:** `{baseUrl}`
- **Official documentation:** [Create Lead](https://www.advantshop.net/api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `Description` | body | `string` | no | Lead description. |
| `FirstName` | body | `string` | no | Lead first name. AdvantShop requires at least one of FirstName, Email, or Phone. |
| `Email` | body | `string` | no | Lead email. AdvantShop requires at least one of FirstName, Email, or Phone. |
| `Phone` | body | `string` | no | Lead phone. AdvantShop requires at least one of FirstName, Email, or Phone. |
