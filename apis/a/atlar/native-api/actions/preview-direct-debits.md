# Preview direct debits with Atlar

Previews direct debits in Atlar.

## Endpoint

- **Method:** `POST`
- **Path:** `/payments/v2beta/direct-debit-batches:preview`
- **Base URL:** `https://api.atlar.com`
- **Official documentation:** [Preview direct debits](https://docs.atlar.com/reference/post-payments-v2beta-direct-debit-batches-preview)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `treatment` | body | `string<string>` | yes |
| `payments[]` | body | `array<object>` | yes |
