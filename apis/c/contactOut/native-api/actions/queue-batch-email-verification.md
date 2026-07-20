# Queue Batch Email Verification with ContactOut

Creates a batch email verification job in ContactOut.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/email/verify/batch`
- **Base URL:** `https://api.contactout.com`
- **Official documentation:** [Queue Batch Email Verification](https://api.contactout.com/#bulk)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `callback_url` | body | `string` | no | Optional callback URL for async bulk verification results. |
| `emails` | body | `string` | yes | An array of email addresses to verify in bulk. Send multiple values as a array. |
