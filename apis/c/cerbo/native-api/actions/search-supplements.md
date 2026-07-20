# Search Supplements with Cerbo

Finds supplements in Cerbo by search terms.

## Endpoint

- **Method:** `GET`
- **Path:** `/supplements/search/:terms`
- **Base URL:** `https://{tenant}.md-hq.com/api/v1`
- **Official documentation:** [Search Supplements](https://docs.cer.bo/#tag/Supplements/operation/searchSupplements)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `terms` | path | `string` | no | You can enter several terms with spaces between each (make sure to url-encode the search string, so spaces would be %20). Each term is treated as potentially a wildcard search so “vitam%20D” (“vitam D”) would return “Vitamin D”, “Vitamin D1000”, etc. |
| `active_only` | query | `boolean` | no | If this parameter is set it will only include ACTIVE supplements |
| `vendor_code` | query | `string` | no | If this parameter is set it will only supplements with matching vendor code (note, this is different from the external_ref_id). |
| `class` | query | `string` | no | If this parameter is set it will only supplements with that class specified |
| `external_ref_id` | query | `string` | no | If this parameter is set it will only include items with the designated external identifier - generally you will want to make this unique so it only includes a single item. |
