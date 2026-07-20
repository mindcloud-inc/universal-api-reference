# Get Full Results by Pod ID with Wolfram Alpha

Retrieves Wolfram Alpha results for a specific pod ID.

## Endpoint

- **Method:** `GET`
- **Path:** `/v2/query`
- **Base URL:** `https://api.wolframalpha.com`
- **Official documentation:** [Get Full Results by Pod ID](https://products.wolframalpha.com/api/documentation)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `input` | query | `string` | yes |
| `podid` | query | `string` | yes |
