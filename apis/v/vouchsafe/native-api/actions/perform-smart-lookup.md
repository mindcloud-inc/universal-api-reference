# Perform Smart Lookup with Vouchsafe

Runs smart lookup checks in Vouchsafe.

## Endpoint

- **Method:** `POST`
- **Path:** `/smart-lookups`
- **Base URL:** `https://app.vouchsafe.id/api/v1`
- **Official documentation:** [Perform Smart Lookup](https://app.vouchsafe.id/docs)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `first_name` | body | `string` | yes | Given name(s). |
| `last_name` | body | `string` | yes | Family name. |
| `checks[]` | body | `array<string>` | yes | The background checks to run. Accepted values: `AML`, `CreditBureau`, `OnlineFootprint`. |
| `first_line_of_address` | body | `string` | no | Required when checks includes Credit Bureau. |
| `postcode` | body | `string` | no | Required when checks includes Credit Bureau. |
| `email` | body | `string` | no | Either email or phone is required when checks includes Online Footprint. |
| `phone` | body | `string` | no | Either email or phone is required when checks includes Online Footprint. |
| `date_of_birth` | body | `string` | no | Required when checks includes Credit Bureau or AML. |
| `thresholds` | body | `object` | no | Optional custom thresholds for AML and Online Footprint checks. |
| `thresholds.aml` | body | `number` | no | Minimum score required to pass AML check (0-100). |
| `thresholds.onlineFootprint` | body | `number` | no | Minimum score required to pass Online Footprint check (0-100). |
| `alerts_enabled` | body | `boolean` | no | When true, enables ongoing AML monitoring for this lookup. |
