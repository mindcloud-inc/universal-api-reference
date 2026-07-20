# Get All Campaigns with Ringg AI

Retrieves campaigns from Ringg AI.

## Endpoint

- **Method:** `GET`
- **Path:** `/campaign/all`
- **Base URL:** `https://prod-api.ringg.ai/ca/api/v0`
- **Official documentation:** [Get All Campaigns](https://docs.ringg.ai/api-reference/endpoint/campaign/get-all-campaigns)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `call_count` | query | `boolean` | no | Whether to include call count for each campaign (default: true). |
