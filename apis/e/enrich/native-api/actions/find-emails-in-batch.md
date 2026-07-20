# Find Emails in Batch with Enrich.so

Creates a batch email finder job in Enrich.so.

## Endpoint

- **Method:** `POST`
- **Path:** `/email-finder/batch`
- **Base URL:** `https://dev.enrich.so/api/v3`
- **Official documentation:** [Find Emails in Batch](https://doc.enrich.so/find-emails-in-batch-27483196e0.md)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `leads[]` | body | `array<object>` | yes | Lead objects containing firstName, lastName, and domain. |
| `webhookUrl` | body | `string` | no | Optional callback URL for batch completion. |
