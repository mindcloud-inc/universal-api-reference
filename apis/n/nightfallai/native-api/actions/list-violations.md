# List Violations with Nightfall.ai

Retrieves violations from Nightfall.ai.

## Endpoint

- **Method:** `GET`
- **Path:** `/dlp/v1/violations`
- **Base URL:** `https://api.nightfall.ai`
- **Official documentation:** [List Violations](https://help.nightfall.ai/developer-api/nightfall_apis/saas)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `createdAfter` | query | `number` | no | Unix timestamp in seconds; returns violations created on or after this time. |
| `createdBefore` | query | `number` | no | Unix timestamp in seconds; returns violations created before this time. |
| `updatedAfter` | query | `number` | no | Unix timestamp in seconds; returns violations updated on or after this time. |
