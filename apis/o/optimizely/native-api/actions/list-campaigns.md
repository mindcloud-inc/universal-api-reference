# List Campaigns with Optimizely

Retrieves a list of campaigns from Optimizely.

## Endpoint

- **Method:** `GET`
- **Path:** `/campaigns`
- **Base URL:** `https://api.optimizely.com/v2`
- **Official documentation:** [List Campaigns](https://docs.developers.optimizely.com/web-experimentation/reference/list_campaigns)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `project_id` | query | `string` | yes | Filter campaigns to one project. |
