# Update Supplement with Cerbo

Updates an existing supplement in Cerbo.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/supplements/:supplement_id`
- **Base URL:** `https://{tenant}.md-hq.com/api/v1`
- **Official documentation:** [Update Supplement](https://docs.cer.bo/#tag/Supplements/operation/updateSupplement)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `supplement_id` | path | `number` | no |
| `name` | body | `string` | no |
| `nicknames` | body | `string` | no |
| `vendor_code` | body | `string` | no |
| `description` | body | `string` | no |
| `external_ref_id` | body | `string` | no |
| `inactive` | body | `boolean` | no |
