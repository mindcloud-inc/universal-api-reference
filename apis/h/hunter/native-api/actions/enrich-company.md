# Enrich Company with Hunter

## Endpoint

- **Method:** `GET`
- **Path:** `/companies/find`
- **Base URL:** `https://api.hunter.io/v2`
- **Official documentation:** [Enrich Company](https://hunter.io/api-documentation/v2#company-enrichment)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `domain` | query | `string` | yes | Company domain to enrich. |
| `clearbit_format` | query | `boolean` | no | — |
