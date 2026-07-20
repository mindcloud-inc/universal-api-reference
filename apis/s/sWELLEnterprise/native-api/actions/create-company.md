# Create Company with SWELLEnterprise

Creates a new company in SWELLEnterprise.

## Endpoint

- **Method:** `POST`
- **Path:** `/crm/companies`
- **Base URL:** `https://dashboard.swellsystem.com/api/v1`
- **Official documentation:** [Create Company](https://dashboard.swellsystem.com/docs#crm-companies-POSTapi-v1-crm-companies)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | body | `string` | yes | The company name. |
| `email` | body | `string` | no | The company email. |
| `phone` | body | `string` | no | The company phone. |
| `website` | body | `string` | no | The company website. |
| `address` | body | `string` | no | The company address. |
| `notes` | body | `string` | no | Notes about the company. |
