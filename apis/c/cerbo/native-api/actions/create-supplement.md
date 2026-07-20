# Create Supplement with Cerbo

Creates a new supplement in Cerbo.

## Endpoint

- **Method:** `POST`
- **Path:** `/supplements`
- **Base URL:** `https://{tenant}.md-hq.com/api/v1`
- **Official documentation:** [Create Supplement](https://docs.cer.bo/#tag/Supplements/operation/createSupplement)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `name` | body | `string` | yes |
| `nicknames` | body | `string` | no |
| `vendor_code` | body | `string` | no |
| `description` | body | `string` | no |
| `external_ref_id` | body | `string` | no |
| `inactive` | body | `boolean` | no |
