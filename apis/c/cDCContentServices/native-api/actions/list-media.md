# List Media with CDC Content Services

Retrieves media from CDC Content Services.

## Endpoint

- **Method:** `GET`
- **Path:** `/v2/resources/media`
- **Base URL:** `https://tools.cdc.gov/api`
- **Official documentation:** [List Media](https://tools.cdc.gov/api/docs/info.aspx)

## Capabilities

This operation supports [pagination](../README.md#pagination), [filtering](../README.md#filtering), and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `q` | query | `string` | no | Search topic, name, and description. Use quotes for exact phrase matching. |
| `mediaTypes` | query | `string` | no | Comma-separated media type names, such as HTML, Image, Video, Button, Badge, Widget, or Infographic. |
| `nameContains` | query | `string` | no | Return media whose name contains this value. |
| `topic` | query | `string` | no | Filter media by topic name. |
| `topicIds` | query | `string` | no | Comma-separated CDC topic identifiers. |
| `audience` | query | `string` | no | Filter media by audience name. |
| `languageName` | query | `string` | no | Filter media by language name, such as English or Spanish. |
| `sourceAcronym` | query | `string` | no | Filter media by source acronym, such as CDC. |
