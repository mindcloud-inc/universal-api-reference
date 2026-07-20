# Get Agent Events with CallTrackingMetrics

Retrieves agent event records from CallTrackingMetrics.

## Endpoint

- **Method:** `GET`
- **Path:** `/accounts/:accountId/agents/events.json`
- **Base URL:** `https://api.calltrackingmetrics.com/api/v1`
- **Official documentation:** [Get Agent Events](https://www.postman.com/ctm-8695/calltrackingmetrics-s-public-workspace/request/e4cd4dd/agent-events)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `user_id` | query | `string` | yes | The internal CTM user ID for the agent whose events should be returned. |
| `start_time` | query | `number` | yes | Start of the event window in epoch seconds. |
| `end_time` | query | `number` | yes | End of the event window in epoch seconds. |
