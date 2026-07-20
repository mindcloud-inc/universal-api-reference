# Get Sentiment Analysis Result with Rev AI

Retrieves a sentiment analysis result from Rev AI.

## Endpoint

- **Method:** `GET`
- **Path:** `/sentiment_analysis/v1/jobs/:id/result`
- **Base URL:** `https://api.rev.ai`
- **Official documentation:** [Get Sentiment Analysis Result](https://docs.rev.ai/api/sentiment-analysis/reference)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Accept` | `application/vnd.rev.sentiment.v1.0+json` |

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `id` | path | `string` | yes |
