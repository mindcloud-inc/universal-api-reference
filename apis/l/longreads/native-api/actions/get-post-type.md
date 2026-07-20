# Get Post Type with Longreads

Retrieves a post type definition from Longreads.

## Endpoint

- **Method:** `GET`
- **Path:** `/wp/v2/types/{type}`
- **Base URL:** `https://longreads.com/wp-json`
- **Official documentation:** [Get Post Type](https://longreads.com/wp-json/wp/v2/types)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `type` | path | `string` | yes | The post type slug to retrieve, such as post. |
