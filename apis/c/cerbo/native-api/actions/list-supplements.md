# List Supplements with Cerbo

Retrieves supplement records from Cerbo.

## Endpoint

- **Method:** `GET`
- **Path:** `/supplements`
- **Base URL:** `https://{tenant}.md-hq.com/api/v1`
- **Official documentation:** [List Supplements](https://docs.cer.bo/#tag/Supplements/operation/listSupplements)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `active_only` | query | `boolean` | no | If this parameter is set it will only include ACTIVE supplements |
| `vendor_code` | query | `string` | no | If this parameter is set it will only supplements with matching vendor code (note, this is different from the external_ref_id). |
| `class` | query | `string` | no | If this parameter is set it will only supplements with that class specified |
| `external_ref_id` | query | `string` | no | If this parameter is set it will only include items with the designated external identifier - generally you will want to make this unique so it only includes a single item. |
