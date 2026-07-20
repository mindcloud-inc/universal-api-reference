# Create Glossary with Amberscript

Creates a new glossary in Amberscript.

## Endpoint

- **Method:** `POST`
- **Path:** `/glossary`
- **Base URL:** `https://api.amberscript.com/api`
- **Official documentation:** [Create Glossary](https://amberscript.github.io/api-docs/#create-a-glossary)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | body | `string` | yes | Name of the glossary. |
| `names[]` | body | `array<string>` | no | Optional array of people, places, or organization names. |
| `items[]` | body | `array<object>` | no | Optional array of glossary items with `name` and `description`. |
