# Create Bulk Job with Sniffmail

Creates a bulk email verification job in Sniffmail.

## Endpoint

- **Method:** `POST`
- **Path:** `/jobs`
- **Base URL:** `https://api.sniffmail.io`
- **Official documentation:** [Create Bulk Job](https://sniffmail.io/docs)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `emails[]` | body | `array<string>` | yes | Provide one or more email addresses for Sniffmail to verify in this bulk job. |
| `webhookUrl` | body | `string` | no | Optionally send the completed-job notification to this webhook URL. |
