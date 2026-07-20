# Get Short Answer with Wolfram Alpha

Retrieves a short text answer from Wolfram Alpha.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/result`
- **Base URL:** `https://api.wolframalpha.com`
- **Official documentation:** [Get Short Answer](https://products.wolframalpha.com/short-answers-api/documentation)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `i` | query | `string` | yes | Question or expression to answer with a single short textual result. |
| `timeout` | query | `number` | no | Maximum processing time in seconds. |
| `units` | query | `string` | no | Measurement system to use: metric or imperial. |
