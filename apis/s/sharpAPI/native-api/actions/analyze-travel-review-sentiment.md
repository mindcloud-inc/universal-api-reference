# Analyze Travel Review Sentiment with SharpAPI

Creates a travel review sentiment job in SharpAPI.

## Endpoint

- **Method:** `POST`
- **Path:** `/tth/review_sentiment`
- **Base URL:** `https://sharpapi.com/api/v1`
- **Official documentation:** [Analyze Travel Review Sentiment](https://sharpapi.com/en/catalog/ai/travel-tourism-hospitality/travel-review-sentiment-checker)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `content` | body | `string` | yes | Provide review text to analyze the sentiment. |
