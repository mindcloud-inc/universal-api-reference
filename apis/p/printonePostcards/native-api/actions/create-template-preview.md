# Create Template Preview with Print.one Postcards

Creates a new template preview in Print.one Postcards.

## Endpoint

- **Method:** `POST`
- **Path:** `/v2/templates/preview/[:id]/[:version]`
- **Base URL:** `https://api.print.one`
- **Official documentation:** [Create Template Preview](https://api.print.one/docs/v2#operation/Template/createTemplatePreview)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | Template ID. |
| `version` | path | `number` | yes | Template version. |
| `asPdf` | query | `boolean` | no | Return the preview as PDF. |
| `firstName` | body | `string` | yes | Merge variable for the template preview. |
