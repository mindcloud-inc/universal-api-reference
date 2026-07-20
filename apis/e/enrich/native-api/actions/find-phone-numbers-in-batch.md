# Find Phone Numbers in Batch with Enrich.so

Creates a bulk phone lookup job in Enrich.so.

## Endpoint

- **Method:** `POST`
- **Path:** `/reverse-lookup/phones/bulk`
- **Base URL:** `https://dev.enrich.so/api/v3`
- **Official documentation:** [Find Phone Numbers in Batch](https://doc.enrich.so/find-phone-numbers-in-batch-27483200e0.md)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `emails[]` | body | `array<string>` | no | Email addresses to use for bulk phone lookup. Provide at least one email address or LinkedIn URL. |
| `linkedins[]` | body | `array<string>` | no | LinkedIn profile URLs to use for bulk phone lookup. Provide at least one email address or LinkedIn URL. |
| `webhookUrl` | body | `string` | no | Optional callback URL for batch completion. |
