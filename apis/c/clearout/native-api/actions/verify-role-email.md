# Verify Role Email with Clearout

Retrieves role email verification results from Clearout.

## Endpoint

- **Method:** `POST`
- **Path:** `/email/verify/role`
- **Base URL:** `https://api.clearout.io/v2`
- **Official documentation:** [Verify Role Email](https://docs.clearout.io/developers/api/email-verify)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `email` | body | `string` | yes |
| `timeout` | body | `number` | no |
