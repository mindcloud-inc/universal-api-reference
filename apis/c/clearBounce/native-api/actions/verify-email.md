# Verify Email with ClearBounce

Verifies a single email address in ClearBounce.

## Endpoint

- **Method:** `POST`
- **Path:** `/verify`
- **Base URL:** `https://api.clearbounce.net/api/v1`
- **Official documentation:** [Verify Email](https://docs.clearbounce.net/api-reference/single-verification)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `email` | body | `string` | yes | The email address to verify with ClearBounce. |
