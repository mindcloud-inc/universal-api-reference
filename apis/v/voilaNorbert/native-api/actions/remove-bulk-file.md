# Remove Bulk File with VoilaNorbert

Deletes a bulk file from VoilaNorbert.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/massives/:id`
- **Base URL:** `https://api.voilanorbert.com/2018-01-08`
- **Official documentation:** [Remove Bulk File](https://api.voilanorbert.com/2018-01-08/#bulk-search-endpoint-bulk-item-operations-delete)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | The bulk file id to remove. |
| `recursive` | body | `boolean` | no | When true, remove related lists and contacts too. |
