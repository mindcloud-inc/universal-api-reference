# List Inflected Forms with Tisane Labs

Retrieves inflected forms from Tisane Labs.

## Endpoint

- **Method:** `GET`
- **Path:** `/lm/inflections`
- **Base URL:** `https://api.tisane.ai`
- **Official documentation:** [List Inflected Forms](https://docs.tisane.ai/apis/tisane-api-short#tag/Language-Model-Direct-Access/operation/inflections)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `language` | query | `string` | yes | Code of a language in Tisane, for example en. |
| `lexeme` | query | `string` | yes | ID of the lexeme to inspect. |
| `family` | query | `string` | yes | ID of the family to inspect. |
