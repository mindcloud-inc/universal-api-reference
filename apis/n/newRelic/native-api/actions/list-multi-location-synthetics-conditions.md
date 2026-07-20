# List Multi-Location Synthetics Conditions with New Relic

Retrieves multi-location synthetics conditions from New Relic.

## Endpoint

- **Method:** `GET`
- **Path:** `/alerts_location_failure_conditions/policies/:policyId.json`
- **Base URL:** `https://api.newrelic.com/v2`
- **Official documentation:** [List Multi-Location Synthetics Conditions](https://docs.newrelic.com/docs/alerts/scale-automate/rest-api/rest-api-calls-alerts/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `policyId` | path | `number` | yes | New Relic alert policy ID. |
