# Verify Catch-All Email with Clearout

Retrieves catch-all email verification results from Clearout.

## Endpoint

- **Method:** `POST`
- **Path:** `/email/verify/catchall`
- **Base URL:** `https://api.clearout.io/v2`
- **Official documentation:** [Verify Catch-All Email](https://docs.clearout.io/developers/api/email-verify)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `email` | body | `string` | yes |
| `timeout` | body | `number` | no |
