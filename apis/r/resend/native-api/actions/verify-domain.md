# Verify Domain with Resend

Triggers verification for an existing domain in Resend.

## Endpoint

- **Method:** `POST`
- **Path:** `/domains/:id/verify`
- **Base URL:** `https://api.resend.com`
- **Official documentation:** [Verify Domain](https://resend.com/docs/api-reference/domains/verify-domain)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | The domain ID (UUID) to verify |
