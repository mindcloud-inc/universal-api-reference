# List Top Answerers For Tag with Stackoverflow

Retrieves top answerers for a tag from Stackoverflow.

## Endpoint

- **Method:** `GET`
- **Path:** `/tags/[:tag]/top-answerers/[:period]`
- **Base URL:** `https://api.stackexchange.com/2.3`
- **Official documentation:** [List Top Answerers For Tag](https://api.stackexchange.com/docs/top-answerers-on-tags)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `tag` | path | `string` | yes | Tag name to analyze. |
| `period` | path | `string` | yes | One of all_time or month. |
| `site` | query | `string` | yes | API site parameter, for example stackoverflow. |
