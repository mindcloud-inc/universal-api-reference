# Transform JSON with 1001fx

Transforms JSON into another structure using a template.

## Endpoint

- **Method:** `POST`
- **Path:** `/data/json2json`
- **Base URL:** `https://api.1001fx.com`
- **Official documentation:** [Transform JSON](https://1001fx.com/functions/json2json)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `inputJson` | body | `object` | no | Input JSON object to transform. |
| `inputJsonString` | body | `string` | no | Input JSON string to transform. |
| `templateJson` | body | `object` | no | Template JSON object that defines the output structure. |
| `templateJsonString` | body | `string` | no | Template JSON string that defines the output structure. |
