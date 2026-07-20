# Validate Emails in Batch with Enrich.so

Creates a batch email validation job in Enrich.so.

## Endpoint

- **Method:** `POST`
- **Path:** `/email-validation/batch`
- **Base URL:** `https://dev.enrich.so/api/v3`
- **Official documentation:** [Validate Emails in Batch](https://doc.enrich.so/validate-emails-in-batch-27483192e0.md)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `emails[]` | body | `array<string>` | yes | Email addresses to validate in batch. |
| `webhookUrl` | body | `string` | no | Optional callback URL for batch completion. |
