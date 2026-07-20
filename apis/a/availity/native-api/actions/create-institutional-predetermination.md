# Create Institutional Predetermination with Availity

Creates an institutional predetermination in Availity.

## Endpoint

- **Method:** `POST`
- **Path:** `/availity/v1/institutional-claims`
- **Base URL:** `https://api.availity.com`
- **Official documentation:** [Create Institutional Predetermination](https://developer.availity.com/blog/2025/3/25/hipaa-transactions)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `institutionalClaim` | body | `object` | no | PCE 1.0 institutional claim predetermination request body. |
