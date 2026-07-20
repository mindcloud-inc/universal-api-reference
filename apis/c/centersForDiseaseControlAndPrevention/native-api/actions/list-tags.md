# List Tags with Centers for Disease Control and Prevention

Retrieves tags from CDC Content Services.

## Endpoint

- **Method:** `GET`
- **Path:** `/v2/resources/tags`
- **Base URL:** `https://tools.cdc.gov/api`
- **Official documentation:** [List Tags](https://tools.cdc.gov/api/docs/info.aspx)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `language` | query | `string` | no | Filter tags by language. |
| `nameContains` | query | `string` | no | Return tags whose names contain this text. |
| `typeName` | query | `string` | no | Return tags belonging to this tag type name. |
| `mediaId` | query | `number` | no | Return tags associated with this media ID. |
| `typeId` | query | `number` | no | Return tags belonging to this tag type ID. |
