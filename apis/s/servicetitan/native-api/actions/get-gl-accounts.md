# Get GL Accounts with ServiceTitan

## Endpoint

- **Method:** `GET`
- **Path:** `accounting/v2/tenant/{tenant}/gl-accounts`
- **Base URL:** `https://{baseUrl}/`

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `names` | query | `string` | no | — |
| `numbers` | query | `string` | no | — |
| `ids` | query | `string` | no | — |
| `types` | query | `string` | no | Comma-delimited list of account types, maximum 50 items. |
