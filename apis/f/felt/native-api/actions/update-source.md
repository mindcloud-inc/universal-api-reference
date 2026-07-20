# Update Source with Felt

Updates an existing data source in Felt.

## Endpoint

- **Method:** `POST`
- **Path:** `/sources/:sourceId/update`
- **Base URL:** `https://felt.com/api/v2`
- **Official documentation:** [Update Source](https://developers.felt.com/rest-api/api-reference/sources)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `sourceId` | path | `string` | yes | The Felt source ID. |
| `name` | body | `string` | no | The new source name. |
| `connection` | body | `object` | no | Updated source connection settings. |
| `permissions` | body | `object` | no | Updated source permissions. |
