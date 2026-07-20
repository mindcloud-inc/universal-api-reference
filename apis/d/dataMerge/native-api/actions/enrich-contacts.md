# Enrich Contacts with DataMerge

Starts a DataMerge contact enrichment job.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/contact/enrich`
- **Base URL:** `https://api.datamerge.ai`
- **Official documentation:** [Enrich Contacts](https://api.datamerge.ai/docs)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `contacts[]` | body | `array<object>` | yes | Array of contact objects to enrich. |
| `webhook` | body | `string` | no | — |
