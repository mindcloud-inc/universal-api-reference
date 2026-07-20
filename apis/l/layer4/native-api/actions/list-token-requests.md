# List Token Requests with Layer4

Retrieves token requests from a Layer4 bucket.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v1/buckets/:bucketId/token-requests`
- **Base URL:** `https://www.layer4.app`
- **Official documentation:** [List Token Requests](https://www.layer4.app/api-docs#tag/Token-Requests/operation/TokenRequestsController_findAll)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `bucketId` | path | `string` | yes | The Layer4 bucket identifier. |
| `status[]` | query | `array<string>` | no | Filter token requests by one or more statuses. |
| `type[]` | query | `array<string>` | no | Filter token requests by one or more request types. |
