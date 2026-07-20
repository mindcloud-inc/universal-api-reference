# Verify Email with MyEmailVerifier

Retrieves an email verification result from MyEmailVerifier by address.

## Endpoint

- **Method:** `GET`
- **Path:** `/verifier/validate_single/:email/{apiKey}`
- **Base URL:** `https://client.myemailverifier.com`
- **Official documentation:** [Verify Email](https://myemailverifier.com/real-time-email-verification)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `email` | path | `string` | yes | The email address to verify. |
