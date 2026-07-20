# Create Avalara Account with Commerce Layer

## Endpoint

- **Method:** `POST`
- **Path:** `/api/avalara_accounts`
- **Base URL:** `{coreApiEndpoint}`
- **Official documentation:** [Create Avalara Account](https://docs.commercelayer.io/core-api-reference/avalara_accounts/create)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `data.attributes.commit_invoice` | body | `boolean` | no | Whether Avalara should commit invoices. |
| `data.attributes.company_code` | body | `string` | yes | Avalara company code. |
| `data.attributes.ddp` | body | `boolean` | no | Whether seller is responsible for duty and import tax. |
| `data.attributes.name` | body | `string` | yes | Internal Commerce Layer name for the Avalara account. |
| `data.attributes.password` | body | `string` | yes | Avalara account password. |
| `data.attributes.reference` | body | `string` | no | Optional external reference for the Avalara account. |
| `data.attributes.reference_origin` | body | `string` | no | Optional origin for the reference code. |
| `data.attributes.username` | body | `string` | yes | Avalara account username. |
