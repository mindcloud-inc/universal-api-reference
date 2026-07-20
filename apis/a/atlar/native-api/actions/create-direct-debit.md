# Create direct debit with Atlar

Creates a direct debit in Atlar.

## Endpoint

- **Method:** `POST`
- **Path:** `/payments/v2/direct-debits`
- **Base URL:** `https://api.atlar.com`
- **Official documentation:** [Create direct debit](https://docs.atlar.com/reference/post-payments-v2-direct-debits)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `amount` | body | `string<string>` | yes |
| `scheme` | body | `string<string>` | yes |
| `date` | body | `date<string>` | yes |
| `source` | body | `string<string>` | yes |
| `destination` | body | `object<string>` | yes |
| `reference` | body | `string<string>` | yes |
