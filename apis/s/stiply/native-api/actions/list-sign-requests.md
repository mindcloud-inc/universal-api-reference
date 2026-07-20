# List Sign Requests with Stiply

Retrieves sign requests available in Stiply.

## Endpoint

- **Method:** `GET`
- **Path:** `/v2/sign_requests`
- **Base URL:** `https://api.stiply.nl`
- **Official documentation:** [List Sign Requests](https://app.stiply.nl/api-documentation/v2#tag/sign-requests/operation/GetSignRequests)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `status` | query | `string` | no | When provided, only sign requests with the provided status are fetched. |
