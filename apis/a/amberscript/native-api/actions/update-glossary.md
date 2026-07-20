# Update Glossary with Amberscript

Updates an existing glossary in Amberscript.

## Endpoint

- **Method:** `PUT`
- **Path:** `/glossary/:glossaryId`
- **Base URL:** `https://api.amberscript.com/api`
- **Official documentation:** [Update Glossary](https://amberscript.github.io/api-docs/#update-a-glossary)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `glossaryId` | path | `string` | yes | Glossary to update. |
| `name` | body | `string` | yes | Name of the glossary. |
| `names[]` | body | `array<string>` | no | Optional array of people, places, or organization names. |
| `items[]` | body | `array<object>` | no | Optional array of glossary items with `name` and `description`. |
