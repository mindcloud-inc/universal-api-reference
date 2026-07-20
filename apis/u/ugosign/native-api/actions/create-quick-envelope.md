# Create Quick Envelope with Ugosign

Creates a contact, contract, and envelope in Ugosign.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/envelopes/quick`
- **Base URL:** `https://app.ugosign.com/api`
- **Official documentation:** [Create Quick Envelope](https://app.ugosign.com/api/docs)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `contact.email` | body | `string` | yes |
| `contact.family_name` | body | `string` | no |
| `contact.given_name` | body | `string` | no |
| `contract.file` | body | `file` | yes |
| `contract.title` | body | `string` | yes |
| `envelope.initiator_email` | body | `string` | yes |
| `envelope.level` | body | `string` | yes |
