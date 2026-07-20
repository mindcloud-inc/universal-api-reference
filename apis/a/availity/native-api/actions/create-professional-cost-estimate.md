# Create Professional Cost Estimate with Availity

Creates a professional cost estimate in Availity.

## Endpoint

- **Method:** `POST`
- **Path:** `/availity/v2/patient-cost-estimates/prof`
- **Base URL:** `https://api.availity.com`
- **Official documentation:** [Create Professional Cost Estimate](https://developer.availity.com/blog/2025/3/25/hipaa-transactions)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `professionalClaim` | body | `object` | no | PCE 2.0 professional predetermination request body. |
