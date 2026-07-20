# Get Full Results with Wolfram Alpha

Retrieves full Wolfram Alpha query results.

## Endpoint

- **Method:** `GET`
- **Path:** `/v2/query`
- **Base URL:** `https://api.wolframalpha.com`
- **Official documentation:** [Get Full Results](https://products.wolframalpha.com/api/documentation)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `format` | query | `string` | no | Comma-separated output elements to include, such as plaintext, image, or imagemap. |
| `input` | query | `string` | yes | Natural-language query or computation to send to Wolfram\|Alpha. |
| `output` | query | `string` | no | Return format for the Full Results API, such as XML or JSON. |
| `podstate` | query | `string` | no | Pod state override(s) for interactive result refinements. |
