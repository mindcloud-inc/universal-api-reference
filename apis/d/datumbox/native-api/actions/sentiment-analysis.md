# Sentiment Analysis with Datumbox

Analyzes sentiment for a document in Datumbox.

## Endpoint

- **Method:** `POST`
- **Path:** `/SentimentAnalysis.json`
- **Base URL:** `http://api.datumbox.com/1.0`
- **Official documentation:** [Sentiment Analysis](https://www.datumbox.com/files/API-Documentation-1.0v.pdf)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `text` | body | `string` | yes | The clear text to evaluate for sentiment. |
