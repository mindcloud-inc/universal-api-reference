# Resume Bulk File with VoilaNorbert

Resumes a paused bulk file in VoilaNorbert.

## Endpoint

- **Method:** `POST`
- **Path:** `/massives/:id/resume`
- **Base URL:** `https://api.voilanorbert.com/2018-01-08`
- **Official documentation:** [Resume Bulk File](https://api.voilanorbert.com/2018-01-08/#bulk-search-endpoint-bulk-item-operations-post)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | The bulk file id to resume. |
