# Recognize Query with Wolfram Alpha

Recognizes whether Wolfram Alpha can process a query.

## Endpoint

- **Method:** `GET`
- **Path:** `https://www.wolframalpha.com/queryrecognizer/query.jsp`
- **Base URL:** `https://api.wolframalpha.com`
- **Official documentation:** [Recognize Query](https://products.wolframalpha.com/query-recognizer/documentation)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `i` | query | `string` | yes | Text to evaluate with the Fast Query Recognizer. |
| `mode` | query | `string` | no | Recognition mode: Default or Voice. |
| `output` | query | `string` | no | Recognizer output format: xml or json. |
