# Update Envelope with EnvelopeBudget

## Endpoint

- **Method:** `PATCH`
- **Path:** `/envelopes/:budget_id/:envelope_id`
- **Base URL:** `https://envelopebudget.com/api`
- **Official documentation:** [Update Envelope](https://envelopebudget.com/api/docs)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `budget_id` | path | `string` | yes |
| `envelope_id` | path | `string` | yes |
| `name` | body | `string` | no |
| `note` | body | `string` | no |
