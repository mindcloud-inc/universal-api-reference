# List Collections with Goodbarber eCommerce

## Endpoint

- **Method:** `GET`
- **Path:** `/publicapi/v2/general/catalog/:webzine_id/collection/`
- **Base URL:** `https://commerce.goodbarber.dev`
- **Official documentation:** [List Collections](https://commerce.goodbarber.dev/publicapi/v2/documentation/)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `sort` | query | `string` | no | Sorts the returned collections. Possible values: alpha : ascending alphabetical order alpha_desc : descending alphabetical order first_added : ascending creation date order last_added : descending creation date order |
