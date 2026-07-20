# Get Message Statistics with Wooxy

Retrieves email message statistics from Wooxy.

## Endpoint

- **Method:** `POST`
- **Path:** `v3/mailer/info`
- **Base URL:** `https://api.wooxy.com`
- **Official documentation:** [Get Message Statistics](https://wooxy.com/api-documentation/email/get-message-statistics)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `ids[]` | body | `array<string>` | yes | An array of up to 100 Wooxy message IDs. |
