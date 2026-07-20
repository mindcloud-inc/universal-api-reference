# Validate ID Number with IN-D KYC India

Retrieves ID number validation results from IN-D KYC India.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/validation/`
- **Base URL:** `https://api.kyc.in-d.ai`
- **Official documentation:** [Validate ID Number](https://dev.in-d.ai/api-documentation/#operation/validate_id)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `DOC_TYPE` | body | `string` | yes | Document type to validate, for example Aadhar Card Front. |
| `aadhar` | body | `string` | yes | Aadhaar number to validate. |
