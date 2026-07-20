# Verify Email in Sandbox Mode with QuickEmailVerification

Retrieves a simulated email verification result from QuickEmailVerification.

## Endpoint

- **Method:** `GET`
- **Path:** `/verify/sandbox`
- **Base URL:** `https://api.quickemailverification.com/v1`
- **Official documentation:** [Verify Email in Sandbox Mode](https://docs.quickemailverification.com/email-verification-api/sandbox-mode)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `allowed_ip` | query | `boolean` | no | Optional sandbox flag to simulate IP allowlist failures. |
| `email` | query | `string` | yes | Email address to test against QuickEmailVerification sandbox responses. |
