# List Tags with Goodbarber eCommerce

## Endpoint

- **Method:** `GET`
- **Path:** `/publicapi/v2/general/catalog/:webzine_id/tag/`
- **Base URL:** `https://commerce.goodbarber.dev`
- **Official documentation:** [List Tags](https://commerce.goodbarber.dev/publicapi/v2/documentation/)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `sort` | query | `string` | no | Sorts the returned tags. Possible values: alpha : ascending alphabetical order last_created : descending creation date order most_tagged : sorted by descending number of products using this tag |
