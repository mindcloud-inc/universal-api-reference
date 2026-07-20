# Retrain Sources with GPT Chatbot

Retrains multiple URL sources in GPT Chatbot.

## Endpoint

- **Method:** `POST`
- **Path:** `/data-sources/url/re-scrape`
- **Base URL:** `https://app.gptchatbot.it/api/v1`
- **Official documentation:** [Retrain Sources](https://docs.gptchatbot.it/api-reference/data-sources/retrain)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `uuids[]` | body | `array<string>` | yes | List of URL source UUIDs to retrain. |
