# Remove Dictionary Entry with Sapling

Deletes a dictionary entry from Sapling.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/api/v1/dictionary/:dictionaryEntryId`
- **Base URL:** `https://api.sapling.ai`
- **Official documentation:** [Remove Dictionary Entry](https://sapling.ai/docs/api/dictionary/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `dictionary_entry_id` | path | `string` | yes | UUID of the dictionary entry to remove. |
