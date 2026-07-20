# List Record Requests with Layer4

Retrieves record requests from a Layer4 bucket.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v1/buckets/:bucketId/record-requests`
- **Base URL:** `https://www.layer4.app`
- **Official documentation:** [List Record Requests](https://www.layer4.app/api-docs#tag/Record-Requests/operation/RecordRequestsController_findAll)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `bucketId` | path | `string` | yes | The Layer4 bucket identifier. |
| `status[]` | query | `array<string>` | no | Filter record requests by one or more statuses. |
| `type[]` | query | `array<string>` | no | Filter record requests by one or more request types. |
| `decrypt` | query | `boolean` | no | Return decrypted record requests when available. |
