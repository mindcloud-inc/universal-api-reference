# Verify Gibberish Email with Clearout

Retrieves gibberish email verification results from Clearout.

## Endpoint

- **Method:** `POST`
- **Path:** `/email/verify/gibberish`
- **Base URL:** `https://api.clearout.io/v2`
- **Official documentation:** [Verify Gibberish Email](https://docs.clearout.io/developers/api/email-verify)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `email` | body | `string` | yes |
| `timeout` | body | `number` | no |
