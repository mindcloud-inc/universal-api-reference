# Search Posture Events with Nightfall.ai

Finds posture events in Nightfall.ai by filters.

## Endpoint

- **Method:** `GET`
- **Path:** `/posture/v1/events/search`
- **Base URL:** `https://api.nightfall.ai`
- **Official documentation:** [Search Posture Events](https://help.nightfall.ai/developer-api/nightfall_apis/posture-management-apis)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `query` | query | `string` | yes | Nightfall search query string, for example state:active. |
