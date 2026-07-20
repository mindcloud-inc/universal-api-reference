# List Questions with Stackoverflow

Retrieves questions from Stackoverflow.

## Endpoint

- **Method:** `GET`
- **Path:** `/questions`
- **Base URL:** `https://api.stackexchange.com/2.3`
- **Official documentation:** [List Questions](https://api.stackexchange.com/docs/questions)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `site` | query | `string` | yes | The Stack Exchange site to query, such as stackoverflow. |
| `tagged` | query | `string` | no | Filter questions to a semicolon-delimited set of required tags. |
