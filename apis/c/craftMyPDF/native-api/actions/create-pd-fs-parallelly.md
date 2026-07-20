# Create PDFs parallelly with CraftMyPDF

Creates multiple PDFs in parallel in CraftMyPDF.

## Endpoint

- **Method:** `POST`
- **Path:** `/create-parallel`
- **Base URL:** `https://api.craftmypdf.com/v1`
- **Official documentation:** [Create PDFs parallelly](https://craftmypdf.com/docs/index.html)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `requests[]` | body | `array<object>` | yes |
| `merge` | body | `boolean` | no |
| `merge_expiration` | body | `number` | no |
