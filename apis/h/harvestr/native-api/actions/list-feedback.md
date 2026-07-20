# List Feedback with Harvestr.io

## Endpoint

- **Method:** `GET`
- **Path:** `/feedback`
- **Base URL:** `https://rest.harvestr.io/v1`
- **Official documentation:** [List Feedback](https://developers.harvestr.io/api/list-feedback/)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `created_before` | query | `date` | no | Filter items created before this date (ISO 8601 format) |
| `created_after` | query | `date` | no | Filter items created after this date (ISO 8601 format) |
| `updated_before` | query | `date` | no | Filter items updated before this date (ISO 8601 format) |
| `updated_after` | query | `date` | no | Filter items updated after this date (ISO 8601 format) |
| `messageId` | query | `string` | no | Filter feedback by message ID |
| `discoveryId` | query | `string` | no | Filter feedback by discovery ID |
