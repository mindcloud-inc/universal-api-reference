# Batch Validate Tax IDs with Tax ID Pro

Creates batch tax ID validations in Tax ID Pro.

## Endpoint

- **Method:** `POST`
- **Path:** `/validate`
- **Base URL:** `https://v3.api.taxid.pro`
- **Official documentation:** [Batch Validate Tax IDs](https://taxid.pro/docs/batch-validation)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `validations[]` | body | `array<object>` | yes | Array of tax ID validation objects. Each item must include reference_id, country, and tin; type is optional and may be individual, entity, or vat. |
| `is_irs` | query | `boolean` | no | Set true when country values use IRS country codes instead of ISO country codes. |
