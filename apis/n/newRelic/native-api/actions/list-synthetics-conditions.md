# List Synthetics Conditions with New Relic

Retrieves synthetics conditions from New Relic.

## Endpoint

- **Method:** `GET`
- **Path:** `/alerts_synthetics_conditions.json`
- **Base URL:** `https://api.newrelic.com/v2`
- **Official documentation:** [List Synthetics Conditions](https://docs.newrelic.com/docs/alerts/scale-automate/rest-api/rest-api-calls-alerts/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `policy_id` | query | `number` | yes | Filter synthetics conditions by alert policy ID. |
