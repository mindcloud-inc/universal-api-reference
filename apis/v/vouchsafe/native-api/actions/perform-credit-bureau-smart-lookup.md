# Perform Credit Bureau Smart Lookup with Vouchsafe

Runs a credit bureau smart lookup in Vouchsafe.

## Endpoint

- **Method:** `POST`
- **Path:** `/smart-lookups`
- **Base URL:** `https://app.vouchsafe.id/api/v1`
- **Official documentation:** [Perform Credit Bureau Smart Lookup](https://app.vouchsafe.id/docs)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `first_name` | body | `string` | yes | Given name(s). |
| `last_name` | body | `string` | yes | Family name. |
| `first_line_of_address` | body | `string` | yes | First line of address taken from the postcode lookup results. |
| `postcode` | body | `string` | yes | Postcode used in the postcode lookup. |
| `date_of_birth` | body | `string` | yes | Date of birth in YYYY-MM-DD or ISO 8601 format. |
