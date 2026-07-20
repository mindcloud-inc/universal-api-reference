# Create Batch Verification Job with MailFloss

Creates a batch email verification job in MailFloss.

## Endpoint

- **Method:** `POST`
- **Path:** `/batch-verify`
- **Base URL:** `https://api.mailfloss.com`
- **Official documentation:** [Create Batch Verification Job](https://developers.mailfloss.com/9bbG-reference)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `emails[]` | body | `array<string>` | yes | Email addresses to verify in the batch job. |
| `webhookUrl` | body | `string` | no | Optional webhook URL to receive results when the job completes. |
