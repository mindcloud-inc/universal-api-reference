# Create Product with Salesforge

Creates a product in Salesforge.

## Endpoint

- **Method:** `POST`
- **Path:** `/public/v2/workspaces/:workspaceID/products`
- **Base URL:** `https://api.salesforge.ai`
- **Official documentation:** [Create Product](https://api.salesforge.ai/public/v2/docs)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `workspaceID` | path | `string` | yes | — |
| `product` | body | `object` | no | — |
| `product.name` | body | `string` | no | — |
| `product.internalName` | body | `string` | no | — |
| `product.language` | body | `list` | no | Accepted values: `american_english`, `brazilian_portugese`, `british_english`, `czech`, `danish`, `dutch`, `estonian`, `finnish`, `french`, `german`, `hungarian`, `italian`, `japanese`, `latvian`, `lithuanian`, `norwegian`, `polish`, `romanian`, `russian`, `spanish`, `swedish`, `ukrainian`. |
| `product.industry` | body | `string` | no | — |
| `product.idealCustomerProfile` | body | `string` | no | — |
| `product.pain` | body | `string` | no | — |
| `product.solution` | body | `string` | no | — |
| `product.proofPoints` | body | `string` | no | — |
| `product.costOfInaction` | body | `string` | no | — |
| `translation[]` | body | `array<object>` | no | — |
| `translation[].name` | body | `string` | no | — |
| `translation[].internalName` | body | `string` | no | — |
| `translation[].language` | body | `list` | no | Accepted values: `american_english`, `brazilian_portugese`, `british_english`, `czech`, `danish`, `dutch`, `estonian`, `finnish`, `french`, `german`, `hungarian`, `italian`, `japanese`, `latvian`, `lithuanian`, `norwegian`, `polish`, `romanian`, `russian`, `spanish`, `swedish`, `ukrainian`. |
| `translation[].industry` | body | `string` | no | — |
| `translation[].idealCustomerProfile` | body | `string` | no | — |
| `translation[].pain` | body | `string` | no | — |
| `translation[].solution` | body | `string` | no | — |
| `translation[].proofPoints` | body | `string` | no | — |
| `translation[].costOfInaction` | body | `string` | no | — |
