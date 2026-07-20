# List Linked Questions with Stackoverflow

Retrieves linked questions from Stackoverflow.

## Endpoint

- **Method:** `GET`
- **Path:** `/questions/[:ids]/linked`
- **Base URL:** `https://api.stackexchange.com/2.3`
- **Official documentation:** [List Linked Questions](https://api.stackexchange.com/docs/linked-questions)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `ids` | path | `string` | yes | Semicolon-delimited question IDs to resolve linked questions for. |
| `site` | query | `string` | yes | API site parameter, for example stackoverflow. |
