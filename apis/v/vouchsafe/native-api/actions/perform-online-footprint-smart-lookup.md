# Perform Online Footprint Smart Lookup with Vouchsafe

Runs an online footprint smart lookup in Vouchsafe.

## Endpoint

- **Method:** `POST`
- **Path:** `/smart-lookups`
- **Base URL:** `https://app.vouchsafe.id/api/v1`
- **Official documentation:** [Perform Online Footprint Smart Lookup](https://app.vouchsafe.id/docs)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `first_name` | body | `string` | yes | Given name(s). |
| `last_name` | body | `string` | yes | Family name. |
| `email` | body | `string` | no | Either email or phone is required for Online Footprint. |
| `phone` | body | `string` | no | Either email or phone is required for Online Footprint. |
| `thresholds` | body | `object` | no | Optional custom Online Footprint threshold. |
| `thresholds.onlineFootprint` | body | `number` | no | Minimum score required to pass Online Footprint check (0-100). |
