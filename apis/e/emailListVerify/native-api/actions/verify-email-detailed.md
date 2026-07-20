# Verify Email Detailed with EmailListVerify

Retrieves detailed email deliverability results from EmailListVerify.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/verifyEmailDetailed`
- **Base URL:** `https://api.emaillistverify.com`
- **Official documentation:** [Verify Email Detailed](https://api.emaillistverify.com/api-doc#/Verification%20Endpoints/verifySingleEmailDetailed)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `email` | query | `string` | yes | Email address to verify with detailed metadata. |
