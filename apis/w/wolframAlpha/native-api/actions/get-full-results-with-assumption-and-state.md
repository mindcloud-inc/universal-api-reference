# Get Full Results with Assumption and State with Wolfram Alpha

Retrieves full Wolfram Alpha query results with assumptions and pod state.

## Endpoint

- **Method:** `GET`
- **Path:** `/v2/query`
- **Base URL:** `https://api.wolframalpha.com`
- **Official documentation:** [Get Full Results with Assumption and State](https://products.wolframalpha.com/api/documentation)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `assumption` | query | `string` | yes |
| `input` | query | `string` | yes |
| `podstate` | query | `string` | yes |
