# Email Verifier with Tomba

Verifies an email address in Tomba.

## Endpoint

- **Method:** `GET`
- **Path:** `/email-verifier`
- **Base URL:** `https://api.tomba.io/v1`
- **Official documentation:** [Email Verifier](https://docs.tomba.io/api/verifier#email-verifier)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `email` | query | `string` | yes | Email address to verify. |
| `enrich_mobile` | query | `boolean` | no | Include phone data when available. |
