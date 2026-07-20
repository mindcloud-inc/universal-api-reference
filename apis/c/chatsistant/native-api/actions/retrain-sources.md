# Retrain Sources with Chatsistant

Retrains existing URL sources in Chatsistant.

## Endpoint

- **Method:** `POST`
- **Path:** `/data-sources/url/re-scrape`
- **Base URL:** `https://app.chatsistant.com/api/v1`
- **Official documentation:** [Retrain Sources](https://docs.chatsistant.com/api-reference/data-sources/retrain)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `uuids[]` | body | `array<string>` | yes | List of URL source UUIDs to retrain. |
