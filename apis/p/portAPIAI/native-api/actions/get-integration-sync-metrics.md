# Get Integration Sync Metrics with Port API AI

Retrieves integration sync metrics from Port.

## Endpoint

- **Method:** `GET`
- **Path:** `/integration/:integrationInternalId/syncMetrics`
- **Base URL:** `https://api.port.io/v1`
- **Official documentation:** [Get Integration Sync Metrics](https://docs.port.io/api-reference/get-an-integrations-metrics-and-sync-status)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `integrationInternalId` | path | `string` | yes | The integration internal identifier. |
