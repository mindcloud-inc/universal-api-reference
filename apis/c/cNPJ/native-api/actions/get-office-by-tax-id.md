# Get Office by Tax ID with CNPJá

Retrieves office details by tax ID from CNPJá.

## Endpoint

- **Method:** `GET`
- **Path:** `/office/:taxId`
- **Base URL:** `https://api.cnpja.com`
- **Official documentation:** [Get Office by Tax ID](https://cnpja.com/en/api/reference)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `taxId` | path | `string` | yes | CNPJ number without punctuation. |
