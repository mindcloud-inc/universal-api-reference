# Verify Email List with Easy Email Verification

Retrieves verification results for up to 50 emails in Easy Email Verification.

## Endpoint

- **Method:** `POST`
- **Path:** `/verify`
- **Base URL:** `https://api.easyemailverification.com/v1`
- **Official documentation:** [Verify Email List](https://eev.stoplight.io/docs/eev/ed1e2a4c4e6a1-when-you-have-list-of-emails-to-be-verified)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `emails[]` | body | `array<string>` | yes | List of email addresses to verify. Max size is 50. |
