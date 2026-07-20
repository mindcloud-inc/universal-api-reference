# Start Or Continue Gateway Application with Paycove

Starts or continues a gateway application in Paycove.

## Endpoint

- **Method:** `GET`
- **Path:** `https://paycove.io/continue-gateway-application/:unique_account_id`
- **Base URL:** `https://paycove.io/api/v1`
- **Official documentation:** [Start Or Continue Gateway Application](https://docs.paycove.io/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `unique_account_id` | path | `string` | yes | Paycove account unique_id. |
| `first_name` | query | `string` | no | Override admin user's first name. |
| `last_name` | query | `string` | no | Override admin user's last name. |
| `company` | query | `string` | no | Override company name for the application. |
| `redirect_url` | query | `string` | no | Custom redirect URL after the application. |
| `complete_url` | query | `string` | no | Custom completion URL. |
| `refresh_url` | query | `string` | no | Custom refresh URL. |
