# Update Source with Chatsistant

Updates an existing source in Chatsistant.

## Endpoint

- **Method:** `POST`
- **Path:** `/data-source/:uuid/update`
- **Base URL:** `https://app.chatsistant.com/api/v1`
- **Official documentation:** [Update Source](https://docs.chatsistant.com/api-reference/data-sources/update)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `title` | body | `string` | yes | Updated title for the data source. |
| `uuid` | path | `string` | yes | The source UUID. |
