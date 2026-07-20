# Run Batch Analysis with Ahrefs

## Endpoint

- **Method:** `POST`
- **Path:** `/batch-analysis/batch-analysis`
- **Base URL:** `https://api.ahrefs.com/v3`
- **Official documentation:** [Run Batch Analysis](https://docs.ahrefs.com/en/api/reference/batch-analysis/post-batch-analysis)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `select[]` | body | `array<string>` | yes | Fields to include in the batch analysis response. |
| `targets[]` | body | `array<object>` | yes | Targets to analyze. Each target includes a URL plus mode and protocol. |
| `country` | body | `string` | no | Two-letter ISO 3166-1 alpha-2 country code. |
| `volume_mode` | body | `string` | no | Search volume calculation mode: monthly or average. |
