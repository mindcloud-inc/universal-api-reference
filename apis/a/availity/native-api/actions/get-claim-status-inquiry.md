# Get Claim Status Inquiry with Availity

Retrieves a claim status inquiry from Availity.

## Endpoint

- **Method:** `GET`
- **Path:** `/availity/v1/claim-statuses/{id}`
- **Base URL:** `https://api.availity.com`
- **Official documentation:** [Get Claim Status Inquiry](https://developer.availity.com/blog/2025/3/25/hipaa-transactions)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | Unique response ID from the initial claim status inquiry request. |
