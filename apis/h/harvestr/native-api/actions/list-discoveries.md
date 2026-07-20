# List Discoveries with Harvestr.io

## Endpoint

- **Method:** `GET`
- **Path:** `/discovery`
- **Base URL:** `https://rest.harvestr.io/v1`
- **Official documentation:** [List Discoveries](https://developers.harvestr.io/api/list-discoveries/)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `created_before` | query | `date` | no | Filter items created before this date (ISO 8601 format) |
| `created_after` | query | `date` | no | Filter items created after this date (ISO 8601 format) |
| `updated_before` | query | `date` | no | Filter items updated before this date (ISO 8601 format) |
| `updated_after` | query | `date` | no | Filter items updated after this date (ISO 8601 format) |
| `parentId` | query | `string` | no | Filter discoveries by parent discovery ID |
| `select` | query | `string` | no | Comma-separated list of additional relations to include in response. Available: 'discoveryfields' |
