# Extract With Custom API with Diffbot

Extracts a page with a named Diffbot Custom API.

## Endpoint

- **Method:** `GET`
- **Path:** `/v3/custom`
- **Base URL:** `https://api.diffbot.com`
- **Official documentation:** [Extract With Custom API](https://docs.diffbot.com/reference/custom)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | query | `string` | yes | Custom API name to execute. |
| `url` | query | `string` | yes | Page URL to process with a named Custom API. |
