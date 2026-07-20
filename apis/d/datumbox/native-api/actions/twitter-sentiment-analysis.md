# Twitter Sentiment Analysis with Datumbox

Analyzes sentiment for a tweet in Datumbox.

## Endpoint

- **Method:** `POST`
- **Path:** `/TwitterSentimentAnalysis.json`
- **Base URL:** `http://api.datumbox.com/1.0`
- **Official documentation:** [Twitter Sentiment Analysis](https://www.datumbox.com/files/API-Documentation-1.0v.pdf)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `text` | body | `string` | yes | The tweet text to evaluate for sentiment. |
