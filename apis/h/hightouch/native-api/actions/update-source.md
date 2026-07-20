# Update Source with Hightouch

Updates an existing source in Hightouch.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/sources/{sourceId}`
- **Base URL:** `https://api.hightouch.com/api/v1`
- **Official documentation:** [Update Source](https://api.hightouch.io/api/swagger.json)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | body | `string` | no | The source name. |
| `sourceId` | path | `number` | yes | The source ID. |
| `configuration` | body | `object` | no | Source configuration object for the selected source type. |
