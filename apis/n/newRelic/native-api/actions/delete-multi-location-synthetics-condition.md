# Delete Multi-Location Synthetics Condition with New Relic

Deletes an existing multi-location synthetics condition from New Relic.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/alerts_location_failure_conditions/:conditionId.json`
- **Base URL:** `https://api.newrelic.com/v2`
- **Official documentation:** [Delete Multi-Location Synthetics Condition](https://docs.newrelic.com/docs/alerts/scale-automate/rest-api/rest-api-calls-alerts/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `conditionId` | path | `number` | yes | New Relic alert condition ID. |
