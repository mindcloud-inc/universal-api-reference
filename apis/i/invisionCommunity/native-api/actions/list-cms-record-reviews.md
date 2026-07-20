# List CMS Record Reviews with Invision Community

## Endpoint

- **Method:** `GET`
- **Path:** `/cms/records/:database_id/:record_id/reviews`
- **Base URL:** `{communityBaseUrl}/api`
- **Official documentation:** [List CMS Record Reviews](https://invisioncommunity.com/developers/rest-api/index/)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `database_id` | path | `number` | yes | Database identifier. |
| `record_id` | path | `number` | yes | Record identifier. |
