# Get Spoken Result with Wolfram Alpha

Retrieves a spoken-style text answer from Wolfram Alpha.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/spoken`
- **Base URL:** `https://api.wolframalpha.com`
- **Official documentation:** [Get Spoken Result](https://products.wolframalpha.com/spoken-results-api/documentation)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `i` | query | `string` | yes | Question or expression to answer in spoken sentence form. |
| `timeout` | query | `number` | no | Maximum processing time in seconds. |
| `units` | query | `string` | no | Measurement system to use: metric or imperial. |
