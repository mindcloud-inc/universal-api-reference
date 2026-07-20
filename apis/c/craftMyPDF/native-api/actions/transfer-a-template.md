# Transfer a template with CraftMyPDF

Transfers a template to another CraftMyPDF account.

## Endpoint

- **Method:** `POST`
- **Path:** `/transfer-template-to`
- **Base URL:** `https://api.craftmypdf.com/v1`
- **Official documentation:** [Transfer a template](https://craftmypdf.com/docs/index.html)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `template_id` | body | `string` | yes |
| `team_id` | body | `string` | yes |
