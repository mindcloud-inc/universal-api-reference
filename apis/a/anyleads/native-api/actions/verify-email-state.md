# Verify Email State with Anyleads

Retrieves email verification status from Anyleads.

## Endpoint

- **Method:** `POST`
- **Path:** `/api-product/incoming-webhook/verify-email-state`
- **Base URL:** `https://myapiconnect.com`
- **Official documentation:** [Verify Email State](https://docs.anyleads.com/product/en/api-to-prevent-verify-emails-registration-on-your-service)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `email` | body | `string` | yes | Email address to verify. |
