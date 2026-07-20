# Verify Business Email with Clearout

Retrieves business email verification results from Clearout.

## Endpoint

- **Method:** `POST`
- **Path:** `/email/verify/business`
- **Base URL:** `https://api.clearout.io/v2`
- **Official documentation:** [Verify Business Email](https://docs.clearout.io/developers/api/email-verify)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `email` | body | `string` | yes |
| `timeout` | body | `number` | no |
