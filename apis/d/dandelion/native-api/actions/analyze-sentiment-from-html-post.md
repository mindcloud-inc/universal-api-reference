# Analyze Sentiment From HTML via HTTP POST with Dandelion

Retrieves sentiment from HTML in Dandelion via HTTP POST.

## Endpoint

- **Method:** `POST`
- **Path:** `/datatxt/sent/v1`
- **Base URL:** `https://api.dandelion.eu`
- **Official documentation:** [Analyze Sentiment From HTML via HTTP POST](https://dandelion.eu/docs/api/datatxt/sent/v1/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `html` | query | `string` | yes | HTML to analyze. |
| `lang` | query | `string` | no | Language code to force sentiment analysis language. |
