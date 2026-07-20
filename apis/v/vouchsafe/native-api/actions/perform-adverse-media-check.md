# Perform Adverse Media Check with Vouchsafe

Runs an adverse media check in Vouchsafe.

## Endpoint

- **Method:** `POST`
- **Path:** `/adverse-media`
- **Base URL:** `https://app.vouchsafe.id/api/v1`
- **Official documentation:** [Perform Adverse Media Check](https://app.vouchsafe.id/docs)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `first_name` | body | `string` | yes | Given name. |
| `middle_names` | body | `string` | no | Middle name(s), space-separated. |
| `last_name` | body | `string` | yes | Family name. |
| `location` | body | `string` | no | City, county, or country. Strongly recommended to improve precision. |
| `threshold` | body | `number` | no | Adversity score threshold from 0 to 100. |
