# Record Deployment with New Relic

Records a deployment in New Relic.

## Endpoint

- **Method:** `POST`
- **Path:** `/applications/:appId/deployments.json`
- **Base URL:** `https://api.newrelic.com/v2`
- **Official documentation:** [Record Deployment](https://docs.newrelic.com/docs/apm/apm-ui-pages/events/record-deployments/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `appId` | path | `number` | yes | New Relic application ID. |
