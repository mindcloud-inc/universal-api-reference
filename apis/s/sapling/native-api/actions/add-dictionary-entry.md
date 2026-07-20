# Add Dictionary Entry with Sapling

Adds a custom dictionary entry in Sapling.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/dictionary`
- **Base URL:** `https://api.sapling.ai`
- **Official documentation:** [Add Dictionary Entry](https://sapling.ai/docs/api/dictionary/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `entry` | body | `string` | yes | Word or phrase to add to the dictionary. |
| `case_sensitive` | body | `boolean` | no | Whether the dictionary entry should be treated as case-sensitive. |
