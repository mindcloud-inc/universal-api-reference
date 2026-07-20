# Create Source with Hightouch

Creates a new source in Hightouch.

## Endpoint

- **Method:** `POST`
- **Path:** `/sources`
- **Base URL:** `https://api.hightouch.com/api/v1`
- **Official documentation:** [Create Source](https://api.hightouch.io/api/swagger.json)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | body | `string` | yes | The source name. |
| `slug` | body | `string` | yes | The source slug. |
| `type` | body | `string` | yes | The source type, such as snowflake or postgres. |
| `configuration` | body | `object` | yes | Source configuration object for the selected source type. |
