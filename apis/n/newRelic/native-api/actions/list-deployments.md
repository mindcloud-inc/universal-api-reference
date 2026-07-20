# List Deployments with New Relic

Retrieves deployments from New Relic.

## Endpoint

- **Method:** `GET`
- **Path:** `/applications/:appId/deployments.json`
- **Base URL:** `https://api.newrelic.com/v2`
- **Official documentation:** [List Deployments](https://docs.newrelic.com/docs/apm/apm-ui-pages/events/record-deployments/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `appId` | path | `number` | yes | New Relic application ID. |
