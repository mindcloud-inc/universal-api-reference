# Create Tax ID with Quaderno

Creates a registered tax ID in Quaderno.

## Endpoint

- **Method:** `POST`
- **Path:** `/tax_ids`
- **Base URL:** `https://sandbox-quadernoapp.com/api`
- **Official documentation:** [Create Tax ID](https://developers.quaderno.io/api/#tag/Registered-Jurisdictions/operation/createTaxID)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `jurisdiction_id` | body | `number` | yes | Jurisdiction ID to register. |
| `value` | body | `string` | yes | Tax ID value. |
| `valid_from` | body | `date` | no | Start date for validity. |
| `valid_until` | body | `date` | no | End date for validity. |
| `permanent_establishment` | body | `boolean` | no | Whether this is a permanent establishment. |
| `import_scheme` | body | `boolean` | no | Whether the registration uses the import scheme. |
