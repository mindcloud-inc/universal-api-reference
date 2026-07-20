# Update Multi-Location Synthetics Condition with New Relic

Updates an existing multi-location synthetics condition in New Relic.

## Endpoint

- **Method:** `PUT`
- **Path:** `/alerts_location_failure_conditions/:conditionId.json`
- **Base URL:** `https://api.newrelic.com/v2`
- **Official documentation:** [Update Multi-Location Synthetics Condition](https://docs.newrelic.com/docs/alerts/scale-automate/rest-api/rest-api-calls-alerts/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `conditionId` | path | `number` | yes | New Relic alert condition ID. |
