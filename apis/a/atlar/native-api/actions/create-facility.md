# Create facility with Atlar

Creates a facility in Atlar.

## Endpoint

- **Method:** `POST`
- **Path:** `/financial-data/v2beta/facilities`
- **Base URL:** `https://api.atlar.com`
- **Official documentation:** [Create facility](https://docs.atlar.com/reference/post-financial-data-v2beta-facilities)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `lender` | body | `string<string>` | yes |
| `borrowers[]` | body | `array<string>` | yes |
| `commitmentAmount` | body | `object<string>` | yes |
| `terms[]` | body | `array<object>` | yes |
| `timezone` | body | `string<string>` | yes |
