# Verify Email Instantly with Clearout

Retrieves instant email verification results from Clearout.

## Endpoint

- **Method:** `POST`
- **Path:** `/email_verify/instant`
- **Base URL:** `https://api.clearout.io/v2`
- **Official documentation:** [Verify Email Instantly](https://docs.clearout.io/developers/api/email-verify)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `email` | body | `string` | yes | — |
| `timeout` | body | `number` | no | Request wait time (in milliseconds), Maximum allowed wait time should not exceed 180,000 milliseconds |
