# List Users with Harvestr.io

## Endpoint

- **Method:** `GET`
- **Path:** `/user`
- **Base URL:** `https://rest.harvestr.io/v1`
- **Official documentation:** [List Users](https://developers.harvestr.io/api/list-users/)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `created_before` | query | `date` | no | Filter items created before this date (ISO 8601 format) |
| `created_after` | query | `date` | no | Filter items created after this date (ISO 8601 format) |
| `updated_before` | query | `date` | no | Filter items updated before this date (ISO 8601 format) |
| `updated_after` | query | `date` | no | Filter items updated after this date (ISO 8601 format) |
| `email` | query | `string` | no | Filter users by email address |
| `companyId` | query | `string` | no | Filter users by company ID |
| `externalUid` | query | `string` | no | Filter users by external unique identifier |
