# Submit Sentiment Analysis Job with Rev AI

Creates a sentiment analysis job in Rev AI.

## Endpoint

- **Method:** `POST`
- **Path:** `/sentiment_analysis/v1/jobs`
- **Base URL:** `https://api.rev.ai`
- **Official documentation:** [Submit Sentiment Analysis Job](https://docs.rev.ai/api/sentiment-analysis/reference)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `text` | body | `string` | yes |
| `metadata` | body | `string` | no |
| `language` | body | `string` | no |
