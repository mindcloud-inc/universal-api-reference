# List Bounces with Survalyzer

## Endpoint

- **Method:** `POST`
- **Path:** `/publicapi/Distribute/v3/ReadBounceList`
- **Base URL:** `https://api.survalyzer-eu.app`
- **Official documentation:** [List Bounces](https://developer.survalyzer.com/knowledge-base/public-api-eu/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `surveyId` | body | `number` | yes | Survey identifier whose bounce list should be returned. |
| `panelId` | body | `number` | no | Optional panel identifier to scope bounces. |
