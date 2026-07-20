# Query template usage with CraftMyPDF

Retrieves template usage details from CraftMyPDF.

## Endpoint

- **Method:** `GET`
- **Path:** `/query-template-usage`
- **Base URL:** `https://api.craftmypdf.com/v1`
- **Official documentation:** [Query template usage](https://craftmypdf.com/docs/index.html)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `template_ids` | query | `string` | yes |
| `start_date` | query | `date` | no |
| `end_date` | query | `date` | no |
