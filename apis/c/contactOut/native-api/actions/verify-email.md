# Verify Email with ContactOut

Retrieves an email verification result from ContactOut.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/email/verify`
- **Base URL:** `https://api.contactout.com`
- **Official documentation:** [Verify Email](https://api.contactout.com/#single)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `email` | query | `string` | yes | The email address to verify. |
