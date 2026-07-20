# List Topics with Centers for Disease Control and Prevention

Retrieves topics from CDC Content Services.

## Endpoint

- **Method:** `GET`
- **Path:** `/v2/resources/topics`
- **Base URL:** `https://tools.cdc.gov/api`
- **Official documentation:** [List Topics](https://tools.cdc.gov/api/docs/info.aspx)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `language` | query | `string` | no | Comma-separated language names. Defaults to English. |
| `mediaType` | query | `string` | no | Filter topics using media type. |
| `showChild` | query | `boolean` | no | Return sub-topics in the items attribute when true. |
