# Retrain Sources with DONNAJAMES Easy

Retrains URL sources in DONNAJAMES Easy.

## Endpoint

- **Method:** `POST`
- **Path:** `data-sources/url/re-scrape`
- **Base URL:** `https://app.gpt-trainer.com/api/v1`
- **Official documentation:** [Retrain Sources](https://guide.gpt-trainer.com/api-reference/data-sources/retrain)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `uuids[]` | body | `array<string>` | yes | URL data source uuids |
