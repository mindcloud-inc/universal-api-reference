# Verify Free Email with Clearout

Retrieves free email verification results from Clearout.

## Endpoint

- **Method:** `POST`
- **Path:** `/email/verify/free`
- **Base URL:** `https://api.clearout.io/v2`
- **Official documentation:** [Verify Free Email](https://docs.clearout.io/developers/api/email-verify)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `email` | body | `string` | yes |
| `timeout` | body | `number` | no |
