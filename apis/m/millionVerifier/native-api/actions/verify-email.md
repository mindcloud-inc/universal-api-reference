# Verify Email with MillionVerifier

Verifies an email address in MillionVerifier.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v3`
- **Base URL:** `https://api.millionverifier.com`
- **Official documentation:** [Verify Email](https://developer.millionverifier.com/#operation/single-verification)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `email` | query | `string` | yes | Email address to verify in real time. |
| `timeout` | query | `number` | no | Time in seconds before the verification request times out. |
