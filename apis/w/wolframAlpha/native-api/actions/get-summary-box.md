# Get Summary Box with Wolfram Alpha

Retrieves a summary box from Wolfram Alpha.

## Endpoint

- **Method:** `GET`
- **Path:** `https://www.wolframalpha.com/summaryboxes/v1/query`
- **Base URL:** `https://api.wolframalpha.com`
- **Official documentation:** [Get Summary Box](https://products.wolframalpha.com/summary-boxes-api/documentation)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `path` | query | `string` | yes | Summary box path returned by the Fast Query Recognizer or documented path values. |
