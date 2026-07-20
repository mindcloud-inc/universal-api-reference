# Create Envelope with Ugosign

Creates a new envelope in Ugosign.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/envelopes`
- **Base URL:** `https://app.ugosign.com/api`
- **Official documentation:** [Create Envelope](https://app.ugosign.com/api/docs)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `allow_refusal` | body | `string` | no |
| `contract_id` | body | `string` | yes |
| `delivery_mode` | body | `string` | yes |
| `expires_at` | body | `string` | no |
| `initials` | body | `string` | no |
| `initiator_id` | body | `string` | yes |
| `level` | body | `string` | yes |
| `message` | body | `string` | no |
| `recipients` | body | `list<string>` | yes |
| `reminder` | body | `string` | no |
