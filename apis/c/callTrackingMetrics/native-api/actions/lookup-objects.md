# Lookup Objects with CallTrackingMetrics

Retrieves lookup objects for an account from CallTrackingMetrics.

## Endpoint

- **Method:** `GET`
- **Path:** `/accounts/:accountId/lookup.json`
- **Base URL:** `https://api.calltrackingmetrics.com/api/v1`
- **Official documentation:** [Lookup Objects](https://www.postman.com/ctm-8695/calltrackingmetrics-s-public-workspace/request/7t5mc6u/lookup-api)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `object_type` | query | `string` | no | Optional CTM lookup object type to filter the results. |
