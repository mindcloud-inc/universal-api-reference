# Create Synthetics Condition with New Relic

Creates a new synthetics condition in New Relic.

## Endpoint

- **Method:** `POST`
- **Path:** `/alerts_synthetics_conditions/policies/:policyId.json`
- **Base URL:** `https://api.newrelic.com/v2`
- **Official documentation:** [Create Synthetics Condition](https://docs.newrelic.com/docs/alerts/scale-automate/rest-api/rest-api-calls-alerts/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `policyId` | path | `number` | yes | New Relic alert policy ID. |
