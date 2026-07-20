# Validate Single Fuzzy Search Name Input with Verificaremails

Retrieves a fuzzy search name validation result from Verificaremails.

## Endpoint

- **Method:** `GET`
- **Path:** `/fuzzysearch/validate/single`
- **Base URL:** `https://dashboard.verificaremails.com/myapi`
- **Official documentation:** [Validate Single Fuzzy Search Name Input](https://dashboard.verificaremails.com/documentation/index.html?v=6)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `term` | query | `string` | yes | JSON object encoded as a string. Example: {"name":"Name","use_first_names":1,"gender":"M","country":"ES"}. |
