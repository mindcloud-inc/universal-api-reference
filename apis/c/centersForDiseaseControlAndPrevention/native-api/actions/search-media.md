# Search Media with Centers for Disease Control and Prevention

Finds media in CDC Content Services.

## Endpoint

- **Method:** `GET`
- **Path:** `/v2/resources/media`
- **Base URL:** `https://tools.cdc.gov/api`
- **Official documentation:** [Search Media](https://tools.cdc.gov/api/docs/info.aspx)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `audience` | query | `string` | no | Filter media by audience. |
| `languageName` | query | `string` | no | Comma-separated language names. |
| `mediaTypes` | query | `string` | no | Comma-separated media type names. |
| `nameContains` | query | `string` | no | Return media whose name contains this text. |
| `q` | query | `string` | no | Searches topic, name, and description. |
| `sourceAcronym` | query | `string` | no | Filter media by source acronym, such as CDC. |
| `topic` | query | `string` | no | Filter media by topic name. |
| `topicIds` | query | `string` | no | Comma-separated sub-topic IDs. |
| `fields` | query | `string` | no | Comma-separated first-level fields to return. Defaults to a compact useful media summary. |
