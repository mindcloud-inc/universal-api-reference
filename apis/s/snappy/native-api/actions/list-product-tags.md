# List Product Tags with Snappy

Retrieves product tags from Snappy.

## Endpoint

- **Method:** `GET`
- **Path:** `/products/tags`
- **Base URL:** `https://api.snappy.com/public-api/v2`
- **Official documentation:** [List Product Tags](https://docs.snappy.com/reference/getproducttags)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `title` | query | `string` | no | Search string to filter tags by name. |
| `skip` | query | `number` | no | Number of records to skip for pagination. |
| `limit` | query | `number` | no | Maximum number of records to return per page. |
