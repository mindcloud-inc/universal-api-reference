# Look Up Professional Profiles in Batch with Enrich.so

Creates a bulk profile lookup job in Enrich.so.

## Endpoint

- **Method:** `POST`
- **Path:** `/reverse-lookup/bulk-lookup`
- **Base URL:** `https://dev.enrich.so/api/v3`
- **Official documentation:** [Look Up Professional Profiles in Batch](https://doc.enrich.so/look-up-professional-profiles-in-batch-27483204e0.md)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `emails[]` | body | `array<string>` | yes | Email addresses to look up in the bulk profile lookup job. |
| `webhookUrl` | body | `string` | no | Optional callback URL for batch completion. |
