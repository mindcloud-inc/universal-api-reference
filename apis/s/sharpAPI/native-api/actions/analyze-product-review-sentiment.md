# Analyze Product Review Sentiment with SharpAPI

Creates a product review sentiment job in SharpAPI.

## Endpoint

- **Method:** `POST`
- **Path:** `/ecommerce/review_sentiment`
- **Base URL:** `https://sharpapi.com/api/v1`
- **Official documentation:** [Analyze Product Review Sentiment](https://sharpapi.com/en/catalog/ai/e-commerce/product-review-sentiment-checker)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `content` | body | `string` | yes | Provide review text to analyze the sentiment. |
