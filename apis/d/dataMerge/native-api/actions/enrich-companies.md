# Enrich Companies with DataMerge

Starts a DataMerge company enrichment job from one or more domains.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/company/enrich`
- **Base URL:** `https://api.datamerge.ai`
- **Official documentation:** [Enrich Companies](https://api.datamerge.ai/docs)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `domains[]` | body | `array<string>` | yes | Domains to enrich as a batch. |
| `list` | body | `string` | no | List slug to receive enriched companies. |
| `refresh` | body | `boolean` | no | Force a new enrichment when matching records already exist. |
