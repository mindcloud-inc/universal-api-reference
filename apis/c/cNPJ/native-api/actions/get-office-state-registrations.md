# Get Office State Registrations with CNPJá

Retrieves office state registrations from CNPJá.

## Endpoint

- **Method:** `GET`
- **Path:** `/office/:taxId`
- **Base URL:** `https://api.cnpja.com`
- **Official documentation:** [Get Office State Registrations](https://cnpja.com/en/api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `taxId` | path | `string` | yes | CNPJ number without punctuation. |
| `registrations` | query | `string` | yes | Use ORIGIN, ALL, or a comma-separated state list such as PR,RS,SC. |
