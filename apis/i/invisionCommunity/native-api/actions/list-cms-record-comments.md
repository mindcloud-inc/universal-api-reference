# List CMS Record Comments with Invision Community

## Endpoint

- **Method:** `GET`
- **Path:** `/cms/records/:database_id/:record_id/comments`
- **Base URL:** `{communityBaseUrl}/api`
- **Official documentation:** [List CMS Record Comments](https://invisioncommunity.com/developers/rest-api/index/)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `database_id` | path | `number` | yes | Database identifier. |
| `record_id` | path | `number` | yes | Record identifier. |
