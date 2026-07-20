# List Featured Questions with Stackoverflow

Retrieves featured questions from Stackoverflow.

## Endpoint

- **Method:** `GET`
- **Path:** `/questions/featured`
- **Base URL:** `https://api.stackexchange.com/2.3`
- **Official documentation:** [List Featured Questions](https://api.stackexchange.com/docs/featured-questions)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `site` | query | `string` | yes | API site parameter, for example stackoverflow. |
