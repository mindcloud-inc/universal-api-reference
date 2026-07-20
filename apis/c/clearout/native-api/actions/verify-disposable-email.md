# Verify Disposable Email with Clearout

Retrieves disposable email verification results from Clearout.

## Endpoint

- **Method:** `POST`
- **Path:** `/email/verify/disposable`
- **Base URL:** `https://api.clearout.io/v2`
- **Official documentation:** [Verify Disposable Email](https://docs.clearout.io/developers/api/email-verify)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `email` | body | `string` | yes |
| `timeout` | body | `number` | no |
