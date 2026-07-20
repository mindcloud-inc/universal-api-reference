# Add Custom Mapping with Sapling

Adds a custom mapping in Sapling.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/custom_mapping`
- **Base URL:** `https://api.sapling.ai`
- **Official documentation:** [Add Custom Mapping](https://sapling.ai/docs/api/custom-mappings/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `entry` | body | `string` | yes | Word or pattern to match. |
| `mapping` | body | `string` | yes | Replacement text to suggest. |
| `case_sensitive` | body | `boolean` | no | Whether the mapping match is case-sensitive. |
| `description` | body | `string` | no | Optional explanation shown with the mapping. |
