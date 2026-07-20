# Perform AML Smart Lookup with Vouchsafe

Runs an AML smart lookup in Vouchsafe.

## Endpoint

- **Method:** `POST`
- **Path:** `/smart-lookups`
- **Base URL:** `https://app.vouchsafe.id/api/v1`
- **Official documentation:** [Perform AML Smart Lookup](https://app.vouchsafe.id/docs)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `first_name` | body | `string` | yes | Given name(s). |
| `last_name` | body | `string` | yes | Family name. |
| `date_of_birth` | body | `string` | yes | Date of birth in YYYY-MM-DD or ISO 8601 format. |
| `thresholds` | body | `object` | no | Optional custom AML threshold. |
| `thresholds.aml` | body | `number` | no | Minimum score required to pass AML check (0-100). |
| `alerts_enabled` | body | `boolean` | no | When true, enables ongoing AML monitoring for this lookup. |
