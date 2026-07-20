# Get Full Results by Pod Index with Wolfram Alpha

Retrieves Wolfram Alpha results for a specific pod index.

## Endpoint

- **Method:** `GET`
- **Path:** `/v2/query`
- **Base URL:** `https://api.wolframalpha.com`
- **Official documentation:** [Get Full Results by Pod Index](https://products.wolframalpha.com/api/documentation)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `input` | query | `string` | yes |
| `podindex` | query | `number` | yes |
