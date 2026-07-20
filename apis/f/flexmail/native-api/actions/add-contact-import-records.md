# Add Contact Import Records with Flexmail

Adds records to a contact import in Flexmail.

## Endpoint

- **Method:** `POST`
- **Path:** `/contacts/imports/{id}/records`
- **Base URL:** `https://api.flexmail.eu`
- **Official documentation:** [Add Contact Import Records](https://api.flexmail.eu/documentation/#post-/contacts/imports/-id-/records)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | — |
| `records[]` | body | `array<object>` | yes | JSON array of contact import records. |
