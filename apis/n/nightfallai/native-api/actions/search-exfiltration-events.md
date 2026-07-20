# Search Exfiltration Events with Nightfall.ai

Finds exfiltration events in Nightfall.ai by filters.

## Endpoint

- **Method:** `GET`
- **Path:** `/exfiltration/v1/events/search`
- **Base URL:** `https://api.nightfall.ai`
- **Official documentation:** [Search Exfiltration Events](https://help.nightfall.ai/developer-api/nightfall_apis/exfiltration-prevention-apis)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `query` | query | `string` | yes | Nightfall search query string, for example state:active. |
