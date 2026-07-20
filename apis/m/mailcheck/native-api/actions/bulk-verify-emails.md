# Bulk Verify Emails with Mailcheck

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/verify/bulk`
- **Base URL:** `https://api.mailcheck.dev`
- **Official documentation:** [Bulk Verify Emails](https://api.mailcheck.dev/docs#verify-bulk)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `emails[]` | body | `array<string>` | yes | Up to 100 email addresses to verify in one request. Provide a JSON array of email strings. |
| `webhook_url` | body | `string` | no | Optional HTTPS URL that MailCheck should notify when bulk verification completes. |
