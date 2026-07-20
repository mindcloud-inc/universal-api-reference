# Search Tags with Runrun.it

Finds tags in Runrun.it.

## Endpoint

- **Method:** `GET`
- **Path:** `/tags`
- **Base URL:** `https://runrun.it/api/v1.0`
- **Official documentation:** [Search Tags](https://runrun.it/api/documentation#tags-query-tags)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `search_term` | query | `string` | yes | Search term for tag name. For a given term will be return a list of tags that match fully or partially with tag name. |
