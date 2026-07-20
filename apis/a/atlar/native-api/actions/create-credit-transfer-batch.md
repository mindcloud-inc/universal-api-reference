# Create credit transfer batch with Atlar

Creates a credit transfer batch in Atlar.

## Endpoint

- **Method:** `POST`
- **Path:** `/payments/v2beta/credit-transfer-batches`
- **Base URL:** `https://api.atlar.com`
- **Official documentation:** [Create credit transfer batch](https://docs.atlar.com/reference/post-payments-v2beta-credit-transfer-batches)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `treatment` | body | `string<string>` | yes |
| `payments[]` | body | `array<object>` | yes |
