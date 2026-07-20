# Create Coverage Inquiry with Availity

Creates a coverage inquiry in Availity.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/coverages`
- **Base URL:** `https://api.availity.com`
- **Official documentation:** [Create Coverage Inquiry](https://developer.availity.com/blog/2025/3/25/hipaa-transactions)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `coverage` | body | `object` | no | Coverage inquiry request body. For demo POST scenarios, Availity documents that an empty JSON body may be used. |
