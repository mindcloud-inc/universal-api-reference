# Create Claim Status Inquiry with Availity

Creates a claim status inquiry in Availity.

## Endpoint

- **Method:** `POST`
- **Path:** `/availity/v1/claim-statuses`
- **Base URL:** `https://api.availity.com`
- **Official documentation:** [Create Claim Status Inquiry](https://developer.availity.com/blog/2025/3/25/hipaa-transactions)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `claimStatus` | body | `object` | no | Claim status inquiry request body. For demo POST scenarios, Availity documents that an empty JSON body may be used. |
