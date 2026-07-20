# Validate Query with Wolfram Alpha

Validates whether a Wolfram Alpha query can be processed.

## Endpoint

- **Method:** `GET`
- **Path:** `/v2/validatequery`
- **Base URL:** `https://api.wolframalpha.com`
- **Official documentation:** [Validate Query](https://products.wolframalpha.com/api/documentation)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `input` | query | `string` | yes | Natural-language query to validate before requesting full results. |
