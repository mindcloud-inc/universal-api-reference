# Create direct debit batch with Atlar

Creates a direct debit batch in Atlar.

## Endpoint

- **Method:** `POST`
- **Path:** `/payments/v2beta/direct-debit-batches`
- **Base URL:** `https://api.atlar.com`
- **Official documentation:** [Create direct debit batch](https://docs.atlar.com/reference/post-payments-v2beta-direct-debit-batches)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `treatment` | body | `string<string>` | yes |
| `payments[]` | body | `array<object>` | yes |
