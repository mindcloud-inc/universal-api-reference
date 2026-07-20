# Create mandate with Atlar

Creates a mandate in Atlar.

## Endpoint

- **Method:** `POST`
- **Path:** `/payments/v2/mandates`
- **Base URL:** `https://api.atlar.com`
- **Official documentation:** [Create mandate](https://docs.atlar.com/reference/post-payments-v2-mandates)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `scheme` | body | `string<string>` | yes |
| `externalAccountId` | body | `string<string>` | yes |
| `creditorReference` | body | `string<string>` | yes |
| `mandateReference` | body | `string<string>` | yes |
