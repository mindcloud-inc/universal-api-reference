# Analyze Sentiment From Text via HTTP GET with Dandelion

Retrieves sentiment from text in Dandelion via HTTP GET.

## Endpoint

- **Method:** `GET`
- **Path:** `/datatxt/sent/v1`
- **Base URL:** `https://api.dandelion.eu`
- **Official documentation:** [Analyze Sentiment From Text via HTTP GET](https://dandelion.eu/docs/api/datatxt/sent/v1/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `text` | query | `string` | yes | Text to analyze. |
| `lang` | query | `string` | no | Language code to force sentiment analysis language. |
