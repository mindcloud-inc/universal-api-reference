# Get Office Tax Regime with CNPJá

Retrieves office tax regime details from CNPJá.

## Endpoint

- **Method:** `GET`
- **Path:** `/office/:taxId`
- **Base URL:** `https://api.cnpja.com`
- **Official documentation:** [Get Office Tax Regime](https://cnpja.com/en/api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `taxId` | path | `string` | yes | CNPJ number without punctuation. |
