# Verify Email with EmailListVerify

Retrieves email deliverability status from EmailListVerify.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/verifyEmail`
- **Base URL:** `https://api.emaillistverify.com`
- **Official documentation:** [Verify Email](https://api.emaillistverify.com/api-doc#/Verification%20Endpoints/verifySingleEmail)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `email` | query | `string` | yes | Email address to verify. |
