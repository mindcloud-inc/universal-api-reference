# List Tags with Fabric

Retrieves tags from Fabric.

## Endpoint

- **Method:** `GET`
- **Path:** `/v2/tags`
- **Base URL:** `https://api.fabric.so`
- **Official documentation:** [List Tags](https://developers.fabric.so/api-reference/tag/tags/get/v2/tags)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `limit` | query | `number` | no | Maximum number of tags to return. |
| `name` | query | `string` | no | Filter tags by name. |
| `offset` | query | `number` | no | Number of tags to skip before returning results. |
