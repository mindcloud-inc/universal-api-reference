# Get Violation with Nightfall.ai

Retrieves a violation from Nightfall.ai.

## Endpoint

- **Method:** `GET`
- **Path:** `/dlp/v1/violations/:violationId`
- **Base URL:** `https://api.nightfall.ai`
- **Official documentation:** [Get Violation](https://help.nightfall.ai/developer-api/nightfall_apis/saas)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `violationId` | path | `string` | yes | The UUID of the violation to fetch. |
