# Retain template versions with CraftMyPDF

Updates retained template versions in CraftMyPDF.

## Endpoint

- **Method:** `POST`
- **Path:** `/retain-template-versions`
- **Base URL:** `https://api.craftmypdf.com/v1`
- **Official documentation:** [Retain template versions](https://craftmypdf.com/docs/index.html)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `template_id` | body | `string` | yes |
| `versions[]` | body | `array<number>` | yes |
| `keep` | body | `boolean` | yes |
