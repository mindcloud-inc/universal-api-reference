# Create Multi-Location Synthetics Condition with New Relic

Creates a new multi-location synthetics condition in New Relic.

## Endpoint

- **Method:** `POST`
- **Path:** `/alerts_location_failure_conditions/policies/:policyId.json`
- **Base URL:** `https://api.newrelic.com/v2`
- **Official documentation:** [Create Multi-Location Synthetics Condition](https://docs.newrelic.com/docs/alerts/scale-automate/rest-api/rest-api-calls-alerts/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `policyId` | path | `number` | yes | New Relic alert policy ID. |
