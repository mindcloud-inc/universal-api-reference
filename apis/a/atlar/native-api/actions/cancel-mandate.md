# Cancel mandate with Atlar

Cancels a mandate in Atlar.

## Endpoint

- **Method:** `POST`
- **Path:** `/payments/v2/mandates/{id}:cancel`
- **Base URL:** `https://api.atlar.com`
- **Official documentation:** [Cancel mandate](https://docs.atlar.com/reference/post-payments-v2-mandates-id-cancel)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `id` | path | `string<string>` | yes |
| `If-Match` | query | `string<string>` | no |
