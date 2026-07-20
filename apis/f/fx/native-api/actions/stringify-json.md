# Stringify JSON with 1001fx

Converts a JSON object into a string.

## Endpoint

- **Method:** `POST`
- **Path:** `/data/stringifyjson`
- **Base URL:** `https://api.1001fx.com`
- **Official documentation:** [Stringify JSON](https://1001fx.com/functions/stringifyjson)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `json` | body | `object` | yes | JSON object to stringify. |
| `replacer[]` | body | `array<string>` | no | Optional replacer array for stringification. |
| `space` | body | `number` | no | Number of spaces to use for indentation. |
