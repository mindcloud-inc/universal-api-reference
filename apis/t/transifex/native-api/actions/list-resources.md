# List Resources with Transifex

## Endpoint

- **Method:** `GET`
- **Path:** `/resources`
- **Base URL:** `https://rest.api.transifex.com`
- **Official documentation:** [List Resources](https://developers.transifex.com/reference/get_resources.md)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `filter[project]` | query | `string` | yes | Return resources for this project id. |
