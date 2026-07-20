# Get Violation Activity with Nightfall.ai

Retrieves activity for a violation from Nightfall.ai.

## Endpoint

- **Method:** `GET`
- **Path:** `/dlp/v1/violations/:violationId/activity`
- **Base URL:** `https://api.nightfall.ai`
- **Official documentation:** [Get Violation Activity](https://help.nightfall.ai/developer-api/nightfall_apis/saas)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `violationId` | path | `string` | yes | The UUID of the violation whose activity you want to fetch. |
