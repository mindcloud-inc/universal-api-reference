# Create Product with Amark

## Endpoint

- **Method:** `POST`
- **Path:** `/Product/Create`
- **Base URL:** `{environment}`

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | body | `number` | yes | — |
| `sku` | body | `string` | yes | Maximum length: 30. |
| `description` | body | `string` | yes | Maximum length: 150. |
| `type` | body | `string` | yes | Maximum length: 2. |
| `troyOz` | body | `number` | yes | — |
| `weightOz` | body | `number` | yes | — |
| `packageUnits` | body | `number` | yes | — |
| `imageURL` | body | `string` | no | Maximum length: 250. |
